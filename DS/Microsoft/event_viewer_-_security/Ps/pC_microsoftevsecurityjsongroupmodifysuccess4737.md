#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-group-modify-success-4737
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = ["epoch_sec","yyyy-MM-dd HH:mm:ss Z"]
  ExtractionType = json
  Conditions = [ """A security-enabled global group was changed""", """"EventID":4737""",""""Channel":"Security"""" ]
  Fields = [
    """"EventTime":({time}\d{10})""",
    """"Hostname":"({host}[\w.-]+?)"""",
    """"EventID":({event_code}\d+)""",
    """({event_name}A security-enabled global group was changed)""",
    """"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"SubjectDomainName":"({src_domain}({domain}[^"]+))"""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"Keywords":({result}[^,]+)"""
    """"TargetUserName":"({group_name}[^"]+)"""
    """"TargetDomainName":"({group_domain}[^"]+)""",
    """"TargetSid":"({group_id}[^"]+)""",
    """"PrivilegeList":"(-|({privileges}[^"]+))""",
# sam_account_name is removed
    """"SidHistory":"(-|({sid_history}[^"]+))""",
    """"ProcessID":({process_id}\d+)""",
    """"ThreadID":({thread_id}\d+)""",
    """exa_json_path=$.TimeCreated,exa_field_name=time"""
    """exa_json_path=$.Computer,exa_field_name=host"""
    """exa_json_path=$.ProcessID,exa_field_name=process_id"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.Keywords,exa_field_name=result"""
    """exa_json_path=$.Level,exa_field_name=run_level"""
    """exa_regex=({event_name}A security-enabled global group was changed)"""
    """exa_regex=Subject:.+?Account Name:\s+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s+({src_domain}({domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)"""
    """exa_regex=Group: Security ID:\s*({group_id}[^\s]+)"""
    """exa_regex=Group:.+?Group Name:\s*({group_name}[^\s]+)"""
   ]


}
```