#### Parser Content
```Java
{
Name = cisco-cv-cef-alert-trigger-success-anomalydetection
  Vendor = Cisco
  Product = Cisco Cyber Vision
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSz"
  Conditions = [ """CEF:""", """|Cisco|Cyber Vision|""", """cat=Anomaly Detection""", """ cybervision[""" ]
  Fields = [
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,6}[+\-]\d\d:\d\d)\s({host}[\w\-\.]+)\scybervision""",
    """Cisco\|([^\|]+\|){2}({alert_type}[^\|]+)""",
    """Cisco\|([^\|]+\|){3}({alert_name}[^\|]+)""",
    """Cisco\|([^\|]+\|){4}({alert_severity}\d)""",
    """\|cat=({category}[^=]+?)\s\w+=""",
    """\smsg=({additional_info}[^=]+?)\s\w+="""
  ]


}
```