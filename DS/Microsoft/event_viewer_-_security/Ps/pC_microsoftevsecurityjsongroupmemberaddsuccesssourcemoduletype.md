#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-add-success-sourcemoduletype"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ExtractionType = json
  Conditions = [
      """"Message":"A member was added to a security-enabled """
      """"SourceModuleType":"""
   ]
  Fields = [
    """({event_name}A member was added to a security-enabled [\w\s]+ group)""",
    """"EventTime":({time}\d{10})""",
    """"EventTime":\s*"({time}\d{1,4}-\d{1,2}-\d{1,2} \d{1,2}:\d{1,2}:\d{1,2})"""",
    """"Hostname":"({dest_host}({host}[\w\-.]*))""",
    """"EventID":({event_code}[^,]+)""",
    """"RecordNumber":({event_id}[^,]+)""",
    """"Message":"A member was added to a security-enabled ({group_type}[^\s]+) group.""",
    """"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"SubjectDomainName":"({src_domain}({domain}[^"]+))""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"TargetUserName":"({group_name}[^"]+)""",
    """"TargetDomainName":"({group_domain}[^"]+)""",
    """"MemberSid":"(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[^\s"]+))""",
    """"MemberName":"({user_dn}[^"]+)""",
    """"MemberName":"CN\\?=({member}[^,]+),({user_ou}OU\\?=.+?DC\\?=.+?[^"]+)"""
    """exa_regex=({event_name}A member was added to a security-enabled [\w\s]+ group)"""
    """exa_json_path=$.EventTime,exa_field_name=time"""
    """exa_json_path=$.Hostname,exa_field_name=host"""
    """exa_json_path=$.Hostname,exa_field_name=dest_host"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.RecordNumber,exa_field_name=event_id"""
    """exa_regex="Message":"A member was added to a security-enabled ({group_type}[^\s]+) group.""",
    """exa_json_path=$.SubjectUserName,exa_field_name=user"""
    """exa_json_path=$.SubjectUserName,exa_field_name=src_user"""
    """exa_json_path=$.SubjectLogonId,exa_field_name=login_id"""
    """exa_json_path=$.SubjectDomainName,exa_field_name=domain"""
    """exa_json_path=$.SubjectDomainName,exa_field_name=src_domain"""
    """exa_json_path=$.TargetUserName,exa_field_name=group_name"""
    """exa_json_path=$.MemberSid,exa_field_name=account_id"""
    """exa_json_path=$.MemberName,exa_field_name=user_dn"""
    """exa_regex="MemberName":"CN\\?=({member}[^,]+),({user_ou}OU\\?=.+?DC\\?=.+?[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```