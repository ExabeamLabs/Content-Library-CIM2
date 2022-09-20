#### Parser Content
```Java
{
Name = pan-panorama-kv-app-activity-panoramaver
  Vendor = Palo Alto Networks
  Product = Panorama
  ParserVersion = v1.0.0
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,SYSTEM,""", """ PAN-OS """, """Panorama ver""" ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),""",
    """Client IP:\s*({src_ip}[A-Fa-f:\d.]+)""",
    """Server IP:\s*({dest_ip}[A-Fa-f:\d.]+)""",
    """,SYSTEM,({protocol}[^,]+),""",
    """,SYSTEM,([^,]*,){4}({operation}[^,]+),""",
    """,({dest_host}[\w\-.]+)\s*$""",
  ]


}
```