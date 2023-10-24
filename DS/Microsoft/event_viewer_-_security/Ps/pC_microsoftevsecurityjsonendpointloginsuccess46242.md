#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-success-4624-2"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """An account was successfully logged on"""
    """Account Name"""
    """computer_name"""
    """event_id\":4624"""
  ]
  Fields = [
    """@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[\w\-.]+)"""
    """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-]{1,40}\$?))\\?""""
    """SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?""""
    """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}[^\\]+))\\?""""
    """SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?""""
    """event_id\\?"+:({event_code}\d+)"""
    """ProcessName\\?"+:\\?"+(?:|-|({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/":;\s]+?)))\\?""""
    """WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}[^\s\\]+))\\?""""
    """Status\\?"+:\\?"+({result_code}[^\\]+)\\?""""
    """ProcessId\\?"+:\\?"+({process_id}[^:\\]+?)\\?""""
    """LogonProcessName\\?"+:\\?"+({auth_process}[^\s\\]+)\s*\\?""""
    """AuthenticationPackageName\\?"+:\\?"+({auth_package}[^\s\\]+)\\?""""
    """({event_name}An account was successfully logged on)"""
    """LogonType\\?"+:\\?"({login_type}\d+)\\?""""
    """TargetUserName\\?"+:\\?"({user}[\w\.\-]{1,40}\$?)\\?""""
    """TargetDomainName\\?"+:\\?"({domain}[^\s"\\]+)\\?""""
    """IpAddress\\?"+:\\?"(?:-|(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\\?""""
    """TargetUserSid\\?"+:\\?"({user_sid}[^\\]+)\\?""""
  ]
  DupFields = [
    "host->dest_host"
  ]


}
```