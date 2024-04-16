#### Parser Content
```Java
{
Name = symantec-bccas-csv-alert-trigger-success-avservice
  Vendor = Symantec
  Product = Symantec Content Analysis System
  TimeFormat =  "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """avservice[""", """Antivirus Vendor:""" ]
  Fields = [
    """Timestamp: ({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """avservice\[({alert_id}\d+)\]\s+({alert_name}[^,]+)""",
    """avservice\[\d+\]\s+({alert_type}[^,]+)""",
    """Client: (({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^,\s]+))""",
    """URL: ({malware_url}[^,]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```