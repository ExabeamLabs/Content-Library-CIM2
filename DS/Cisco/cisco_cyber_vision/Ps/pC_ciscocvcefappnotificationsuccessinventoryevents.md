#### Parser Content
```Java
{
Name = cisco-cv-cef-app-notification-success-inventoryevents
  Vendor = Cisco
  Product = Cisco Cyber Vision
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSz"
  Conditions = [ """CEF:""", """|Cisco|Cyber Vision|""", """cat=Inventory Events""", """ cybervision[""" ]
  Fields = [
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,6}[+\-]\d\d:\d\d)\s({host}[\w\-\.]+)\scybervision""",
    """Cisco\|([^\|]+\|){2}({operation_type}[^\|]+)""",
    """Cisco\|([^\|]+\|){3}({event_name}[^\|]+)""",
    """Cisco\|([^\|]+\|){4}({severity}\d)""",
    """({app}Cyber Vision)""",
    """\|cat=({category}[^=]+?)\s\w+=""",
    """\smsg=({additional_info}[^=]+?)\s\w+=""",
    """SCVSensorId=({sensor_id}[^\s]+)""",
    """\ssmac=({src_mac}[^\s]+)\s\w+="""
  ]


}
```