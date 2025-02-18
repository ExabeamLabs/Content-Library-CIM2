#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-audit-policy-modify-success-5449
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """"EventID":5449,""", """A Windows Filtering Platform provider context has been changed""", """"Channel":"Security"""" ]
  Fields = ${WindowsParsersTemplates.microsoft-json-events.Fields}[
    """Subject:\s*Security ID:\s*({user_sid}[^:]+?)(\s+\w+){1,2}:\s"""
    """Subject:[^"]+?Account Name:\s*(({domain}[^:\\]+?)\\+)?({user}[^:\\]+?)(\s+\w+){1,2}:\s"""
    """Subject:[^"]+?Account Domain:\s*({domain}[^:]+?)(\s+\w+){1,2}:\s"""
    """Subject:[^"]+?Logon ID:\s*({login_id}[^:]+?)(\s+\w+){1,2}:\s"""
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