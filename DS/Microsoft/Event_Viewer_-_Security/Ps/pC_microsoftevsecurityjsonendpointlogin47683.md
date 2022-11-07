#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-4768-3
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = ["""A Kerberos authentication ticket (TGT) was requested""", """Account Name""", """computer_name""", """event_id\":4768"""]
  Fields = ${DLWindowsParsersTemplates.json-windows-events-2.Fields}[
    """({event_name}A Kerberos authentication ticket \(TGT\) was requested)""",
    """TargetUserName\\?"+:\\?"(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|({user}[^\\]+))\\?"""",
    """IpAddress\\?"+:\\?"(::[\w]+:)?({dest_ip}[a-fA-F:\d.]+)\\?"""",
    """Status\\?"+:\\?"({result_code}[\w\-]+)\\?"""",
    """TargetDomainName\\?"+:\\?"(?:-|({domain}[^\s\\]+?))\\?"""",
    """TargetSid\\?"+:\\?"({user_sid}[^\\]+)\\?""""
  ]
  DupFields = [
    "result_code->failure_code"
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