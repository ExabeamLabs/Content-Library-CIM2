#### Parser Content
```Java
{
Name = microsoft-evapp-json-file-read-success-326
  ParserVersion = v1.0.0
  Product = Event Viewer - Application
  Conditions = [ """"EventID":326,""", """"Channel":"Application"""", """"ProviderName":"""", """The database engine attached a database""" ]
  Fields = ${WindowsParsersTemplates.microsoft-json-events.Fields}[
    """({event_name}The database engine attached a database)""",
    """({operation}The database engine attached a database)\s+\(\d+,\s+({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))))\)\."""  
  ]    
  DupFields = [ "host->dest_host" ] 

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