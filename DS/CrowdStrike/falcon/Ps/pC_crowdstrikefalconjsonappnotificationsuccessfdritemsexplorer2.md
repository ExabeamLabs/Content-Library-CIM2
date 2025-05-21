#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-notification-success-fdritemsexplorer-2
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = "epoch_sec"
  Conditions = [ """destinationServiceName =CrowdStrike""", """dproc=FDR Items explorer""" ]
  Fields = [
    """exa_json_path=$._time,exa_regex=^({time}\d{10})""",
    """exa_json_path=$.Category,exa_field_name=category""",
    """exa_json_path=$.ProductName,exa_field_name=app""",
    """exa_json_path=$.FileName,exa_field_name=file_name""",
    """exa_json_path=$.SHA256HashData,exa_field_name=hash_sha256""",
    """exa_json_path=$.SoftwareType,exa_field_name=app_type""",
    """exa_json_path=$.CompanyName,exa_field_name=company""",
    """exa_json_path=$.hostname,exa_field_name=host""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.externalIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.cid,exa_field_name=cid""",
    """exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.MAC,exa_field_name=src_mac""",
    """exa_json_path=$.InterfaceAlias,exa_field_name=interface"""
  ]
  ParserVersion = "v1.0.0"


}
```