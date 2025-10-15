#### Parser Content
```Java
{
Name = "zeek-z-json-file-read-success-fuid"
  Vendor = "Zeek"
  Product = "Zeek"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
   """files","""
   """"fuid":"""
   """"conn_uids":"""
  ]
  Fields = [
    """exa_json_path=$._system_name,exa_field_name=host""",
    """exa_json_path=$.ts,exa_field_name=time""",
    """exa_json_path=$.tx_hosts[:1],exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.rx_hosts[:1],exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.conn_uids[:1],exa_field_name=connection_uid""",
    """exa_json_path=$.source,exa_field_name=protocol""",
    """exa_json_path=$.source,exa_field_name=log_source""",
    """exa_json_path=$.analyzers,exa_field_name=analyzers""",
    """exa_json_path=$.mime_type,exa_field_name=mime""",
    """exa_json_path=$.seen_bytes,exa_field_name=bytes""",
    """exa_json_path=$.total_bytes,exa_field_name=bytes""",
    """exa_json_path=$.md5,exa_field_name=hash_md5""",
    """exa_json_path=$.sha1,exa_field_name=hash_sha1""",
    """exa_regex="filename":"({src_file_name}[^"]+?(\.({file_ext}\w+))?)"""",
    """exa_json_path=$.fuid,exa_field_name=file_id""",
  ]
  ParserVersion = "v1.0.0"


}
```