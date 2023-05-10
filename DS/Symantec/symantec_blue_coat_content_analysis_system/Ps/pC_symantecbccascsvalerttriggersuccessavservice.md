#### Parser Content
```Java
{
Name = symantec-bccas-csv-alert-trigger-success-avservice
  Vendor = Symantec
  Product = Symantec Blue Coat Content Analysis System
  TimeFormat =  "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """avservice[""", """Antivirus Vendor:""" ]
  Fields = [
    """Timestamp: ({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """avservice\[({alert_id}\d+)\]\s+({alert_name}[^,]+)""",
    """avservice\[\d+\]\s+({alert_type}[^,]+)""",
    """Client: (({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^,\s]+))""",
    """URL: ({malware_url}[^,]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```