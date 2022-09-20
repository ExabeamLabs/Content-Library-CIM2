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
      """TargetUserName:({user}[^,]+)""",
      """TargetDomainName:({domain}[^,]+)""",
      """TargetLogonId:({login_id}[^,]+)""",
      """TargetUserSid:({user_sid}[^,]+)""",
      """LogonProcessName:({auth_process}[^,]+)""",
      """AuthenticationPackageName:({auth_package}[^,]+)""",
      """WorkstationName:(-|({src_host_windows}[^,]+))""",
      """SubjectUserSid:({subject_sid}[^,]+)""",
      """SubjectUserName:(-|({caller_user}[^,]+))""",
      """KeyLength:(({key_length}\d+))""",
      """\sProcessName:(?:-|({process_path}({process_dir}[^,]*?[\\\/]+)?({process_name}[^,\\\/]+))),"""
      """IpAddress:({src_ip}[A-Fa-f\d:.]+)""",
      """IpPort:({src_port}\d+)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```