#### Parser Content
```Java
{
Name = "tanium-cp-json-alert-trigger-success-eventprocess"
  ExtractionType = json
  Vendor = "Tanium"
  Product = "Tanium Core Platform"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
   """trace_process_table_id"""
   """Timestamp"""
   """Computer Name"""
   """Computer IP"""
  ]
  Fields = [
    """exa_json_path=$.Timestamp,exa_field_name=time"""
    """exa_json_path=$.['User Name'],exa_field_name=user"""
    """exa_json_path=$.['User Id'],exa_field_name=user"""
    """exa_json_path=$.['User Domain'],exa_field_name=domain"""
    """exa_json_path=$.['Event Name'],exa_field_name=alert_name"""
    """exa_json_path=$.['Event Name'],exa_field_name=alert_type"""
    """exa_json_path=$.Priority,exa_field_name=alert_severity"""
    """exa_json_path=$.['Computer Name'],exa_field_name=src_host"""
    """exa_json_path=$.['Event Id'],exa_field_name=alert_id"""
    """exa_json_path=$.['Computer IP'],exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_regex="fullpath\\":\\"({malware_url}[^"]+?)\\*""""
    """exa_regex="name\\":\\"({file_name}[^"]+?)\\*""""
    """exa_regex="md5\\":\\"({hash_md5}[^"]+?)\\*""""
    """exa_regex="payload=\{({additional_info}.+?[^\\]")\}"""
    """exa_regex="user\\?":\\?"(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]
  ParserVersion = "v1.0.0"


}
```