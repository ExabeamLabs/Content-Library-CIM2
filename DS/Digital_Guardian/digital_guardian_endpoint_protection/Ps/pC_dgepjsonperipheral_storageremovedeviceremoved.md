#### Parser Content
```Java
{
Name = dg-ep-json-peripheral_storage-remove-deviceremoved
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "epoch"
  ExtractionType = json
  Conditions = [ """"_time":""", """"Event Display Name":"""", """"Device Removed"""" ]
  Fields = [
    """exa_json_path=$._time,exa_field_name=time"""
    """exa_regex="Computer Name\":\"([^\\\/]+?[\\\/]+)?({host}[^\"]+)"""
    """exa_json_path=$.User,exa_field_name=user"""
    """exa_json_path=$.['Process Domain'],exa_field_name=web_domain"""
    """exa_json_path=$.['Process PID'],exa_field_name=process_id"""
    """exa_json_path=$.Application,exa_field_name=app"""
    """exa_json_path=$.['MD5 Hash'],exa_field_name=hash_md5"""
    """exa_json_path=$.['SHA1 Hash'],exa_field_name=hash_sha1"""
    """exa_json_path=$.['Event Display Name'],exa_field_name=operation"""
    """exa_json_path=$.['Process Path'],exa_regex=({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+))"""
  ]
  ParserVersion = "v1.0.0"


}
```