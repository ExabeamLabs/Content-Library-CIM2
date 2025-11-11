#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-success-4624"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Conditions = [
    """"EventID":4624"""
    """"AuthenticationPackageName":""""
  ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s"""
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"@timestamp"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""
    """TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
    """"Computer":"({dest_host}({host}[\w\-.]+))"""
    """({event_name}An account was successfully logged on)"""
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"EventReceivedTime":\s*({time}\d+)"""
    """"timestamp":\s*({time}\d+)"""
    """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""""
    """"(Hostname|MachineName|hostname)":"({dest_host}({host}[\w\-.]*))"""
    """({event_code}4624)"""
    """"LogonType":"?({login_type}\d+)"""
    """"TargetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"TargetDomainName":"({dest_domain}({domain}[^"]*))"""
    """"ProcessName":"(?:-|({process_path}[^"]*))"""
    """"IpAddress":"(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
    """"hostip":"(?:-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
    """"LogonProcessName":"(-|({auth_process}.+?))\s*""""
    """"AuthenticationPackageName":"(-|({auth_package}[^"]*))"""
    """"TargetLogonId":"({dest_login_id}({login_id}[^"]*))"""
    """"TargetUserSid":"({dest_user_sid}({user_sid}[^"]*))"""
    """Workstation Name:((?-i)\\+[rnt])*\s*(|([A-Fa-f:\d.]+|-|({src_host_windows}[^\\\s]+?))\s*((?-i)\\+[rnt])*)?Source"""
    """"WorkstationName":"(?:|[A-Fa-f:\d.]+|-|({src_host_windows}[^"]+))""""
    """"KeyLength":"?({key_length}\d+)"?,"""
    """"SubjectUserSid":"({subject_sid}[^"]+)"""
    """"Process":"(-|({process_name}[^"]+))""""
  ]


}
```