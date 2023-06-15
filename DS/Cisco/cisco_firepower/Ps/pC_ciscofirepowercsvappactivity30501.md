#### Parser Content
```Java
{
Name = cisco-firepower-csv-app-activity-30501
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""FTD""", """30501"""]
  Fields = [
    """eventTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """(\w{3} \d\d \d\d:\d\d:\d\d)\s+({host}[\w\.-]+)\s*%FTD""",
    """({time}\w+ \d+ \d+ \d\d:\d\d:\d\d)\s*({host}[\w\-.]+)?""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """\d{6}:\s*({event_name}[^;]+?);\s*Connection for udp src outside:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+).+?dst outside:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+)"""
    """\d{6}:\s*({event_name}.+?({protocol}\w+)\s*translation)\sfrom"""
    """from\s*({src_interface}[^:]+):(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_port}\d+)(\([^\s)]+\))?\s*to\s*({dest_interface}[^:]+):(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```