#### Parser Content
```Java
{
Name = symantec-s-str-printer-activity-success-faxincident
Vendor = "Symantec"
Product = "Symantec"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Endpoint Printer/Fax INCIDENT"""
]
Fields = [
  """({host}[\w\-.]+)\s+DLP_PROD"""
  """\WURL\s+({additional_info}.+?)\s+FILE_NAME"""
  """\WFILE_NAME\s+({object}.+?)\s+MACHINE_NAME"""
  """\WMACHINE_NAME\s+({src_host}[\w\-.]+)"""
  """\WUSER_NAME\s+(({domain}[^\\\s]+)\\+)?({full_name}.+?)\s+APP_NAME"""
  """\WAPP_NAME\s+({app}.+?)\s+MACHINE_IP"""
  """\WMACHINE_IP\s+({src_ip}[A-Fa-f:\d.]+)"""
]
ParserVersion = "v1.0.0"


}
```