#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-app-notification-success-productname"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ExtractionType = json
  Conditions = [ """"ProductName":""", """"Category":""", """"destinationServiceName":"CrowdStrike"""", """"_time":""" ]
  TimeFormat = ["epoch_sec"]
  Fields = [
    """exa_json_path=$.ProductName,exa_field_name=additional_info""",
    """exa_json_path=$.['_time'],exa_regex=({time}\d{10})""",
    """exa_json_path=$.destinationServiceNam,exa_field_name=app""",
    """exa_json_path=$.hostname,exa_field_name=host""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.cid,exa_field_name=cid""",
    """exa_json_path=$.FileName,exa_regex=({file_name}[^"$]+?(\.({file_ext}[^\."$]+))?)$""",
    """exa_json_path=$.externalIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.dproc,exa_field_name=dproc""",
    """exa_json_path=$.SHA256HashData,exa_field_name=hash_sha256"""
  ]
  ParserVersion = "v1.0.0"


}
```