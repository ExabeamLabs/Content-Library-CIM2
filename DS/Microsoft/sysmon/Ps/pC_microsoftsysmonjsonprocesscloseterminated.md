#### Parser Content
```Java
{
Name = microsoft-sysmon-json-process-close-terminated
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd HH:mm:ss.SSS"]
  Conditions = [ """Microsoft-Windows-Sysmon""", """Process terminated:""", """"AccountName":"""" ]
  Fields = [
    """exa_json_path=$.UtcTime,exa_field_name=time"""
    """exa_regex="Image":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """exa_json_path=$.Domain,exa_field_name=domain"""
    """exa_json_path=$.AccountName,exa_field_name=user"""
    """exa_json_path=$.AccountName,exa_field_name=user"""
    """exa_json_path=$.Hostname,exa_field_name=host"""
    """exa_json_path=$.Hostname,exa_field_name=dest_host"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.ProcessGuid,exa_field_name=process_guid"""
    """exa_json_path=$.ProcessID,exa_field_name=process_id"""
    """exa_regex=({log_name}Microsoft-Windows-Sysmon)"""

  ]


}
```