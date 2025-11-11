#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-fail-4625-2
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = ["""An account failed to log on""", """Failure Reason""", """event_id\":4625""", """computer_name"""]
  Fields = ${WindowsParsersTemplates.json-windows-events-2-aa.Fields}[
    """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
    """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}[^\\]+))\\?"""",
    """(?:winlog\.)?computer_name\\?"+:\\?"+({dest_host}({host}[\w\-.]+))""",
    """WorkstationName\\?"+:\\?"+(?:-|({src_host}({src_host_windows}[^\s\\]+)))\\?"""",
    """({event_name}An account failed to log on)""",
    """SubjectUserName\\?"+:\\?"(?:-|LOCAL SYSTEM|({src_user}[^\\]+))\\?"""",
    """SubjectDomainName\\?"+:\\?"(?:-|NT AUTHORITY|({src_domain}[^\\]+))\\?"""",
    """TargetUserSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\]+))\\?"""",
    """TargetUserName\\?"+:\\?"+(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+)))?)|({user_upn}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?)))\\?"""",
    """TargetDomainName\\?"+:\\?"(?:-|\.|NT AUTHORITY| |({dest_domain}({domain}[^\s\\]+?)))\\?"""",
    """IpAddress\\?"+:\\?"(?:-|(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """SubStatus\\?"+:\\?"+({failure_code}({result_code}[^\\]+))\\?"""
  ]

json-windows-events-2-aa = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?"""",
    """SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?"""",
    """event_id\\?"+:({event_code}\d+)""",
    """ProcessName\\?"+:\\?"+(?:|-|({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/":;\s]+?)))\\?"""",
    """Status\\?"+:\\?"+({result_code}[^\\]+)\\?"""",
    """ProcessId\\?"+:\\?"+({process_id}[^:\\]+?)\\?"""",
    """LogonProcessName\\?"+:\\?"+({auth_process}[^\s\\]+)\s*\\?"""",
    """AuthenticationPackageName\\?"+:\\?"+({auth_package}[^\s\\]+)\\?""""
  
}
```