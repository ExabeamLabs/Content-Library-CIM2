#### Parser Content
```Java
{
Name = symantec-dlp-kv-peripheral-storage-insert-success-devicewas
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Device Manager Message""", """device was""", """successfully""", """User: """ ]
  Fields = [
    """(\s|,)({dest_host}[^,\s]+),Device Manager Message""",
    """,Local: (0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """Begin:\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """User:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?),Domain""",
    """(?i)({operation}device was allowed successfully)""",
    """Domain:\s+({domain}[^,]+),""",
    """\[class\]:(?:\?|({device_class}.+?))\s+\[guid\]:""",
    """Device ID:\s+({device_id}.+)&\d+""",
    """\[deviceID\]:({device_id}.+)&\d+""",
    """The device was allowed successfully\.\s+({operation_details}.*?)\s+\[guid""",
    """The device was Allowed successfully\.\s+({operation_details}[^,]+?),""",
    """VEN_({device_vid}[^&]+)&(amp;)?PROD_({device_pid}[^\\&]+)"""
  ]
  SOAR {
    IncidentType = "generic"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "operation_details->description"]
    NameTemplate = """Symantec ${device_class} insert found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="dest_address", Fields=["dest_host->host_name", "dest_ip->ip_address"]

}
```