#### Parser Content
```Java
{
Name = microsoft-nps-csv-endpoint-login-success-13
  Vendor = Microsoft
  Product = Network Policy Server 
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","IAS",""", """,13,"""]
  Fields = [
    """"({host}[^\,]+)","IAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d,\d*,"({domain}[^\\]+)\\({user}[^"]+)",+?,"({src_ip}[^"]+)",.+?,"({dest_ip}[^"]+)","({src_host}[^"]+)"""",
    """"({dest_host}[^"]+)",\d\d\/\d\d\/\d\d\d\d\s"""
  ]
  ParserVersion = v1.0.0


}
```