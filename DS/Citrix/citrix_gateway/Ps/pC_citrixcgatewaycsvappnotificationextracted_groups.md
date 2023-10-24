#### Parser Content
```Java
{
Name = citrix-cgateway-csv-app-notification-extracted_groups
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ AAA EXTRACTED_GROUPS """ ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT""",
    """GMT\s*({host}[^:\s]+)(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*Extracted_groups\s+"""# extracted_group is removed
    """GMT\s*({host}[^:\s]+)(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*Extracted_groups\s+"""# extracted_group is removed
    ]
  DupFields = ["host->src_host"]


}
```