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
    """({result}(Success|Failure) Audit)\s+({host}[^\s]+)\s+Logon""",
	    """({event_code}4648)""",
    """SubjectUserName:(-|({user}[^,]+)),""",
    """SubjectDomainName:(-|({domain}[^,]+)),""",
    """SubjectLogonId:({login_id}[^,]+),""",
    """SubjectUserSid:({user_sid}[^,]+),""",
    """TargetUserName:({account}[^,]+),""",
    """TargetDomainName:({account_domain}[^,]+),""",
    """TargetServerName:({dest_host}[^,]+),""",
    """TargetInfo:({dest_service_name}[^,]+),""",
    """TargetLogonGuid:({account_login_guid}[^,]+),""",
    """\sLogonGuid:({user_login_guid}[^,]+),""",
    """ProcessId:({process_id}[^,]+),""",
    """ProcessName:({process_path}({process_dir}([^,]+)[\\\/])?({process_name}[^,\\]+?)),\s+\w+:""",
    """IpAddress:(::ffff:)?({src_ip}[a-fA-F\d:.]+),""",
    """IpPort:({src_port}\d+),"""
  ]


}
```