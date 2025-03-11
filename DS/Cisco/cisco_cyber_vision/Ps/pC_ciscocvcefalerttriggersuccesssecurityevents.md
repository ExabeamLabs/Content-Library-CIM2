#### Parser Content
```Java
{
Name = cisco-cv-cef-alert-trigger-success-securityevents
  Vendor = Cisco
  Product = Cisco Cyber Vision
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSz"
  Conditions = [ """CEF:""", """|Cisco|Cyber Vision|""", """cat=Security Events""", """ cybervision[""" ]
  Fields = [
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,6}[+\-]\d\d:\d\d)\s({host}[\w\-\.]+)\scybervision""",
    """Cisco\|([^\|]+\|){2}({alert_type}[^\|]+)""",
    """Cisco\|([^\|]+\|){3}({alert_name}[^\|]+)""",
    """Cisco\|([^\|]+\|){4}({alert_severity}\d)""",
    """\|cat=({category}[^=]+?)\s\w+=""",
    """\smsg=({additional_info}[^=]+?)\s\w+=""",
    """SCVSensorIp=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """SCVSensorId=({sensor_id}[^\s]+)"""
  ]


}
```