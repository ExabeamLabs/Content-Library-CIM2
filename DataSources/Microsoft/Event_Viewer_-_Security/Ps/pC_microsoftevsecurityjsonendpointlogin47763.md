#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-4776-3
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = ["""attempted to validate the credentials for an account""", """Authentication Package""", """computer_name""", """event_id\":4776""", """"audit-event""""]
  Fields = ${DLWindowsParsersTemplates.json-windows-events-2.Fields}[
    """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)""",
    """The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials""",
    """Workstation\\?"+:\\?"+({dest_host}[^\\]+)\\?"""",
    """TargetUserName\\?"+:\\?"+((({user}[^@\s\\]+?)(?:@({domain}[^\\]+))?)|({email_address}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?))\\?""""
  ]

json-windows-events-2 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[^\\]+)""",
    """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[^\\]+))\\?"""",
    """SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?"""",
    """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}[^\\]+))\\?"""",
    """SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?"""",
    """event_id\\?"+:({event_code}\d+)""",
    """ProcessName\\?"+:\\?"+(?:|-|({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/":;\s]+?)))\\?"""",
    """WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}[^\s\\]+))\\?"""",
    """Status\\?"+:\\?"+({result_code}[^\\]+)\\?"""",
    """ProcessId\\?"+:\\?"+({process_id}[^:\\]+?)\\?"""",
    """LogonProcessName\\?"+:\\?"+({auth_process}[^\s\\]+)\s*\\?"""",
    """AuthenticationPackageName\\?"+:\\?"+({auth_package}[^\s\\]+)\\?""""
  
}
```