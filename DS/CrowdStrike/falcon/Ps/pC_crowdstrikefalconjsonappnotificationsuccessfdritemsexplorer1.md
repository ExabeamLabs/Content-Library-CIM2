#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-notification-success-fdritemsexplorer-1
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """destinationServiceName =CrowdStrike""", """dproc=FDR Items explorer""", """"EventType":""", """"ScanInfo":""" ]
  Fields = [
    """exa_json_path=$.EventOccurredAt,exa_field_name=time""",
    """exa_json_path=$.EventType,exa_field_name=event_name""",
    """exa_json_path=$..cid,exa_field_name=cid""",
    """exa_json_path=$..ID,exa_field_name=scan_id""",
    """exa_json_path=$..ScanUUID,exa_field_name=scan_id""",
    """exa_json_path=$..source,exa_field_name=log_source""",
    """exa_json_path=$..Repository,exa_field_name=repository_name""",
    """exa_json_path=$..Registry,exa_field_name=registry_details""",
    """exa_json_path=$..OSInfo.Name,exa_field_name=os""",
    """exa_json_path=$..ImageScanEventType,exa_field_name=event_category"""
  ]
  ParserVersion = "v1.0.0"


}
```