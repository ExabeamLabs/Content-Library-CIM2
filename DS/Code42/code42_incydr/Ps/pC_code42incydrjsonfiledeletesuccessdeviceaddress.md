#### Parser Content
```Java
{
Name = code42-incydr-json-file-delete-success-deviceaddress
  Vendor = Code42
  Product = Code42 Incydr
  ExtractionType = json
  TimeFormat = "epoch"
  ParserVersion = "v1.0.0"
  Conditions= [ """formattedTimestamp""", """deviceAddress""", """deviceRemoteAddress""", """operatingSystemUser""", """"fileEventType":""", """"modular_input_consumption_time":"""]
  Fields = [
    """exa_json_path=$.processOwner,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.fileOwnerUsername,exa_regex=(\w+\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.deviceAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.deviceRemoteAddress,exa_regex=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """exa_json_path=$.deviceRemoteAddress,exa_regex=({src_translated_ip}\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4})""",
    """exa_json_path=$.files[0].fileName,exa_field_name=file_name""",
    """exa_json_path=$.files[0].fileEventType,exa_field_name=access""",
    """exa_json_path=$.files[0].fileType,exa_field_name=file_type""",
    """exa_json_path=$.files[0].detectionTimestamp,exa_field_name=time""",
    """exa_regex="processName":\s*"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))"""",
    """exa_json_path=$.files[0],exa_regex="fullPath":\s*"({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
    """exa_json_path=$.files[0].md5,exa_field_name=hash_md5""",
    """exa_json_path=$.files[0].sha256,exa_field_name=hash_sha256""",
    """exa_json_path=$.userUid,exa_field_name=user_uid""",
  ]


}
```