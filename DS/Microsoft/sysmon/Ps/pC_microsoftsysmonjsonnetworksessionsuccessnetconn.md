#### Parser Content
```Java
{
Name = "microsoft-sysmon-json-network-session-success-netconn"
  ExtractionType = json
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Sysmon"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd HH:mm:ss.SSS"]
  Conditions = [
"""Microsoft-Windows-Sysmon"""
"""Network connection detected"""
""""AccountName":""""
  ]
  Fields = [
    """exa_json_path=$.UtcTime,exa_field_name=time"""
    """exa_json_path=$.Protocol,exa_field_name=protocol"""
    """exa_json_path=$.Domain,exa_field_name=domain"""
    """exa_json_path=$.AccountName,exa_field_name=user"""
    """exa_json_path=$.ProcessGuid,exa_field_name=process_guid"""
    """exa_json_path=$.ProcessGuid,exa_field_name=process_guid"""
    """exa_regex=ProcessId:\s*({process_id}\d+)"""
    """exa_json_path=$.Hostname,exa_field_name=host"""
    """exa_json_path=$.Hostname,exa_field_name=dest_host"""
    """exa_json_path=$.SourceIp,exa_field_name=src_ip"""
    """exa_json_path=$.SourceHostname,exa_field_name=src_host"""
    """exa_json_path=$.SourcePort,exa_field_name=src_port"""
    """exa_json_path=$.DestinationIp,exa_field_name=dest_ip"""
    """exa_json_path=$.DestinationHostname,exa_field_name=dest_host"""
    """exa_json_path=$.DestinationHostname,exa_field_name=dest_host"""
    """exa_json_path=$.DestinationPort,exa_field_name=dest_port"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_regex=\"User\":\"((NT AUTHORITY|({domain}[^\\]+))[\\]+)?((?i)SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\""""
    """exa_regex=\"Image\":\"({path}({process_path}({process_dir}[^\"]*?[\\\/]+)?({process_name}[^\"\\\/]+)))\""""
  ]


}
```