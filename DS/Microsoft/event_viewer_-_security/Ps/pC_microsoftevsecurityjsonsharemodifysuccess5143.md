#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-share-modify-success-5143
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """"EventID":5143,""", """"Channel":"Security"""", """"ProviderName":"""" ]
  Fields = ${WindowsParsersTemplates.microsoft-json-events.Fields}[
    """Subject:\s+Security ID:\s+({user_sid}[^\s]+)""",
    """Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Account Domain:\s+({domain}[^\s]+)""",
    """Logon ID:\s+({login_id}[^\s]+)""",  
    """Share Information:\s+Object Type:\s+({file_type}[^:]+?)\s+Share Name:""",
    """Share Name:\s+(?:[\\\*]+)?({share_name}[^\s]+)\s+Share Path:""",
    """Share Path:\s*[\\\?]*({share_path}(({d_parent}[^@]+?)\\)?(|({d_name}[^\\]+?)))\s*Old Remark:"""
  ]

microsoft-json-events {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd HH:mm:ss Z"
  ExtractionType = json
  Fields = [
    """exa_json_path=$.TimeCreated,exa_field_name=time"""
    """exa_json_path=$.ProviderName,exa_field_name=provider_name"""
    """exa_json_path=$.Computer,exa_field_name=host"""
    """exa_json_path=$.Channel,exa_field_name=channel"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.EventRecordID,exa_field_name=event_id"""
    """exa_json_path=$.ThreadID,exa_field_name=thread_id"""
    """exa_json_path=$.Opcode,exa_field_name=opcode"""
    """exa_json_path=$.Level,exa_field_name=run_level"""
    """exa_json_path=$.Keywords,exa_field_name=result"""
    """exa_json_path=$.ActivityID,exa_field_name=activity_id"""
    """exa_json_path=$.ProcessID,exa_field_name=process_id"""
    """exa_json_path=$.Message,exa_field_name=additional_info"""    
    """exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """exa_json_path=$.Message,exa_regex=(S-[^"]+|({event_name}[^\."]+))"""
  
}
```