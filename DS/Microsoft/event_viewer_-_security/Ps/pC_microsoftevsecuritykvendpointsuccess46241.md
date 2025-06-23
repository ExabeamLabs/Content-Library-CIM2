#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-success-4624-1
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = ["""4624""", """LogonType:""","""TargetUserName:""","""Logon"""]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d[+-]\d\d:\d\d)\s({host}[\w\-.]+)"""
      """Audit\s+({host}[\w\-.]+)\s+Logon""",
      """({event_code}4624)""",
      """LogonType:({login_type}\d+)""",
      """TargetUserName:({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """TargetDomainName:({domain}[^,]+)""",
      """TargetLogonId:({login_id}[^,]+)""",
      """TargetUserSid:({user_sid}[^,]+)""",
      """LogonProcessName:({auth_process}[^,]+)""",
      """AuthenticationPackageName:({auth_package}[^,]+)""",
      """WorkstationName:(-|({src_host_windows}[^,]+))""",
      """SubjectUserSid:({subject_sid}[^,]+)""",
      """SubjectUserName:(-|({src_user}[^,]+))""",
      """KeyLength:(({key_length}\d+))""",
      """\sProcessName:(?:-|({process_path}({process_dir}[^,]*?[\\\/]+)?({process_name}[^,\\\/]+))),"""
      """IpAddress:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """IpPort:({src_port}\d+)"""
    ]
    DupFields = [ "src_host_windows->src_host", "login_id->dest_login_id", "user_sid->dest_user_sid" , "domain->dest_domain", "user->dest_user" ]
    ParserVersion = "v1.0.0"
  

}
```