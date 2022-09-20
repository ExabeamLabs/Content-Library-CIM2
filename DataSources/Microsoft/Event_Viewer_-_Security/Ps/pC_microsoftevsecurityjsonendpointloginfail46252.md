#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-fail-4625-2
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = ["""An account failed to log on""", """Failure Reason""", """event_id\":4625""", """computer_name"""]
  Fields = ${DLWindowsParsersTemplates.json-windows-events-2.Fields}[
    """({event_name}An account failed to log on)""",
    """SubjectUserName\\?"+:\\?"(?:-|LOCAL SYSTEM|({caller_user}[^\\]+))\\?"""",
    """SubjectDomainName\\?"+:\\?"(?:-|NT AUTHORITY|({caller_domain}[^\\]+))\\?"""",
    """TargetUserSid\\?"+:\\?"({user_sid}[^\\]+)\\?"""",
    """TargetUserName\\?"+:\\?"+(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|((({user}[^@\s\\]+?)(?:@({domain}[^\\]+))?)|({email_address}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?)))\\?"""",
    """TargetDomainName\\?"+:\\?"(?:-|\.|NT AUTHORITY| |({domain}[^\s\\]+?))\\?"""",
    """IpAddress\\?"+:\\?"(?:-|(::[\w]+:)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
    """SubStatus\\?"+:\\?"+({result_code}[^\\]+)\\?"""
  ]
  DupFields=[ 
    "host->dest_host"
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