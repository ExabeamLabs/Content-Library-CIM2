#### Parser Content
```Java
{
Name = pan-ngfw-json-network-notification-success-iptag
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Conditions = [  """LogType":"IPTAG""", """TagName":""", """"MappingDataSource":""", """"SourceIP":""" ]
  Fields = [
    """exa_json_path=$.TimeGenerated,exa_field_name=time"""
    """exa_json_path=$.DeviceName,exa_field_name=host"""
    """exa_json_path=$.TagName,exa_field_name=tag"""
    """exa_json_path=$.MappingDataSource,exa_field_name=additional_info"""
    """exa_json_path=$.SourceIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
   ]
  ParserVersion = "v1.0.0"


}
```