#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-switch-success-4648-4
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """Microsoft-Windows-Security-Auditing""","""SubjectUserName:""", """TargetUserName:""", """4648""", """TargetServerName:""", """Logon""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d{1,3}[+\-]+\d\d:\d\d""",
    """({result}(Success|Failure) Audit)\s+({host}[\w\-.]+)\s+Logon""",
	    """({event_code}4648)""",
    """SubjectUserName:(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),""",
    """SubjectDomainName:(-|({domain}[^,]+)),""",
    """SubjectLogonId:({login_id}[^,]+),""",
    """SubjectUserSid:({user_sid}[^,]+),""",
    """TargetUserName:({dest_user}[^,]+),""",
    """TargetDomainName:({dest_domain}[^,]+),""",
    """TargetServerName:({dest_host}[\w\-.]+),""",
    """TargetInfo:({dest_service_name}[^,]+),""",
    """TargetLogonGuid:({account_login_guid}[^,]+),""",
    """\sLogonGuid:({user_login_guid}[^,]+),""",
    """ProcessId:({process_id}[^,]+),""",
    """ProcessName:({process_path}({process_dir}([^,]+)[\\\/])?({process_name}[^,\\]+?)),\s+\w+:""",
    """IpAddress:(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """IpPort:({src_port}\d+),"""
  ]
  DupFields = [ "dest_user->account" ]


}
```