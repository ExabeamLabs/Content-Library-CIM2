#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-activity-success-4691
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """"EventID":4691,""", """"Channel":"Security"""", """"ProviderName":"""" ]  
  Fields = ${WindowsParsersTemplates.microsoft-json-events.Fields}[
    """Subject:\s+Security ID:\s+({user_sid}[^\s]+)""",
    """Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Account Domain:\s+({domain}[^\s]+)""",
    """Logon ID:\s+({login_id}[^\s]+)""", 
    """Object Type:\s*({operation_type}[^"]+?)\s*Object Name:""",
    """Object Name:\s*({object}[^"]+?)\s*Process Information:""",
    """Object Name:\s*({file_path}({file_dir}(?:[^"]+)?[\\\/])?({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\."]+?))))\s*Process Information:""",
    """Accesses:\s*({access}[^"]+?)\s*Access Mask:""" 
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