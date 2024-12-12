#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-notification-4627
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"EventID":4627,""", """"Message":"Group membership information""" ]
  Fields = [
    """({event_name}Group membership information)""",
    """({event_code}4627)""",
    """"(Hostname|Computer)"+:"+({host}[^",]+)""",
    """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"SubjectUserSid"+:"+(SYSTEM|NT AUTHORITY|\\NULL SID|({user_sid}[^"]+))""",
    """"SubjectUserName"+:"+(-|({account_name}[^"]+))""",
    """"SubjectDomainName"+:"+(-|({account_domain}[^"]+))""",
    """"SubjectLogonId"+:"+({login_id}[^"]+)""",
    """"TargetUserSid"+:"+(SYSTEM|ANONYMOUS|({user_sid}[^",]+))""",
    """"TargetUserName"+:"+(SYSTEM|ANONYMOUS|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"TargetDomainName"+:"+(NT AUTHORITY|({domain}[^"]+))""",
    """"TargetLogonId"+:"+({login_id}[^"]+)""",
    """"LogonType"+:"+({login_type}\d+)""",
# sequence_num is removed
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s"""
    """exa_json_path=$.Message,exa_field_name=event_name"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.Hostname,exa_field_name=host"""
    """exa_json_path=$.Computer,exa_field_name=host"""
    """exa_regex="EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """exa_json_path=$..SubjectUserSid,exa_field_name=user_sid"""
    """exa_json_path=$..SubjectUserName,exa_regex=(-|({account_name}[^"]+))"""
    """exa_json_path=$..SubjectDomainName,exa_regex=(-|({account_domain}[^"]+))"""
    """exa_json_path=$..SubjectLogonId,exa_field_name=login_id"""
    """exa_json_path=$..TargetUserSid,exa_field_name=user_sid"""
    """exa_json_path=$..TargetUserName,exa_field_name=user"""
    """exa_json_path=$..TargetDomainName,exa_field_name=domain"""
    """exa_json_path=$..TargetLogonId,exa_field_name=login_id"""
    """exa_json_path=$..LogonType,exa_field_name=login_type"""
  ]


}
```