#### Parser Content
```Java
{
Name = symantec-dlp-kv-peripheral-storage-insert-success-allowedthedevice
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Device Manager Message""", """Allowed the device""", """User: """ ]
  Fields = [
    """SymantecServer:\s*({host}[\w\-.]+)""",
    """(\s|,)({dest_host}[^,\s]+),Device Manager Message""",
    """,Local: (0\.0\.0\.0|({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
    """Begin:\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """User:\s+({user}.+?),Domain""",
    """({operation}Allowed the device)""",
    """Domain:\s+({domain}[^,]+),""",
    """\[class\]:(?:\?|({device_type}.+?))\s+\[guid\]:""",
    """Device ID:\s+({device_id}.+)&\d+""",
    """\[deviceID\]:({device_id}.+)&\d+""",
    """Allowed the device\.\s+({activity_details}.*?)\s+\[guid"""
  ]
  SOAR {
    IncidentType = "generic"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "activity_details->description"]
    NameTemplate = """Symantec ${device_type} insert found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="dest_address", Fields=["dest_host->host_name", "dest_ip->ip_address"]

}
```