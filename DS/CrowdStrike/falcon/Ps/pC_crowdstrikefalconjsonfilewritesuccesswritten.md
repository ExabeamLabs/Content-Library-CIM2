#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-file-write-success-written
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = v1.0.0
  ExtractionType = json
  TimeFormat = ["epoch", "epoch_sec"]
  Conditions = [ """"aip":""", """"aid":""", """"IsOnRemovableDisk":"1"""", """"event_simpleName":""", """Written"""" ]
  Fields = [
    """"timestamp":"({time}\d{10,13})"""",
    """"UserName":"({user}[\w\.\-]{1,40}\$?)"""",
    """"aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"name":"({event_name}[^"]+)"""",
    """"event_simpleName":"({event_code}[^"]+)"""",
    """"TargetFileName":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?\s*({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\.]+?)))?))\s*"""",
    """"Size":"({bytes}\d+)"""",
    """"DiskParentDeviceInstanceId":"({device_id}[^"]+)"""",
    """"aid":"({aid}[^"]+)""""
    """"aip":"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)""""
    """"ContextProcessId":"({process_guid}[^"]+)""""
    """"event_platform":"({os}[^"]+)""""
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.UserName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))""",
    """exa_json_path=$.aip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.name,exa_field_name=event_name""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
    """exa_regex="TargetFileName":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?\s*({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\.]+?)))?))\s*"""",    """exa_json_path=$.Size,exa_field_name=bytes""",
    """exa_json_path=$.DiskParentDeviceInstanceId,exa_field_name=device_id""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.aip,exa_regex=({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex="((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)"""",
    """exa_json_path=$.ContextProcessId,exa_field_name=process_guid""",
    """exa_json_path=$.event_platform,exa_field_name=os"""
  ]
  DupFields = [ "device_id->service_type" ]


}
```