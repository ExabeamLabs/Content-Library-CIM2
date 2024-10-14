#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-member-list-4799
  ExtractionType = json
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss yyyy", "yyyy-MM-dd HH:mm:ss", "MM/dd/yyyy hh:mm:ss a"]
  ParserVersion = "v1.0.0"
  Conditions = [ """4799""", """A security-enabled local group membership was enumerated""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))""",
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)""",
    """({event_code}4799)""",
    """(?i)\w+\s+\d+\s+\d+:\d+:\d+\s+(am|pm|\d{4}|({host}[\w\-.]+))\s""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s""",
    """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({event_name}A security-enabled local group membership was enumerated)""",
    """Subject:\s*[^"]+?Security ID:\s*({user_sid}[^\s]+)\s+Account Name:""",
    """Subject:\s*[^"]+?Account Name:\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+\s\w+:""",
    """Subject:\s*[^"]+?Account Domain:\s*(-|({domain}[^\s]+))""",
    """Subject:\s*[^"]+?Logon ID:\s*({login_id}[^\s]+)""",
    """Group:\s*[^"]+?Security ID:\s+({group_id}[^\s]+)""",
    """Group:\s*[^"]+?(Group|Account) Name:\s+({group_name}.+?)?\s+(Group|Account) Domain:""",
    """Group:\s*[^"]+?(Group|Account) Domain:\s+({group_domain}[^\s]+)""",
    """Process ID:\s*[^"]+?\s+({process_id}[^\s]+)""",
    """Process Name:\s+({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^\s]+))""",

    """exa_json_path=$.times[0].EventTime,exa_field_name=time"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.Computer,exa_field_name=host"""
    """exa_regex=({event_name}A security-enabled local group membership was enumerated)""",
    """exa_json_path=$..SubjectUserSid,exa_regex=(SYSTEM|({user_sid}\S+))"""
    """exa_json_path=$..SubjectUserName,exa_regex=(SYSTEM|ANONYMOUS LOGON|({user}\S+))"""
    """exa_json_path=$..SubjectDomainName,exa_field_name=domain"""
    """exa_json_path=$..SubjectLogonId,exa_field_name=login_id"""
    """exa_json_path=$..TargetSid,exa_field_name=group_id"""
    """exa_json_path=$..TargetUserName,exa_field_name=group_name"""
    """exa_json_path=$..TargetDomainName,exa_regex=(-|NT AUTHORITY|({group_domain}[^\s\\"]+))"""
    """exa_json_path=$..CallerProcessId,exa_field_name=process_id"""
    """exa_json_path=$..CallerProcessName,exa_regex=({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$"""
  ]


}
```