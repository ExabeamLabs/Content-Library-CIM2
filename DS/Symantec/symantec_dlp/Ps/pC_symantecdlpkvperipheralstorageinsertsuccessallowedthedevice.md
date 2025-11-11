#### Parser Content
```Java
{
Name = symantec-dlp-kv-peripheral-storage-insert-success-allowedthedevice
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Device Manager Message""", """Allowed the device""", """,User""", """ [deviceID]:""" ]
  Fields = [
    """SymantecServer:\s*({host}[\w\-.]+)""",
    """(\s|,)({dest_host}[^,\s]+),("Event Description: )?Device Manager Message""",
    """,Local( Host IP)?: (0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """Begin:\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """User( Name)?:\s+(none|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),Domain""",
    """({operation}Allowed the device)""",
    """Domain( Name)?:\s+({domain}[^,]+),""",
    """\[class\]:(?:\?|({device_class}.+?))\s+\[guid\]:""",
    """Device ID:\s+({device_id}.+)&\d+""",
    """\[deviceID\]:({device_id}[^,"]+?)"*,""",
    """Allowed the device\.\s+({operation_details}.*?)\s+\[guid""",
    """VEN_({device_vid}[^&]+)&(amp;)?PROD_({device_pid}[^\\&]+)"""
  ]
  SOAR {
    IncidentType = "generic"
    NameTemplate = """Symantec ${device_class} insert found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="dest_address", Fields=["dest_host->host_name", "dest_ip->ip_address"]

}
```