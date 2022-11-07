#### Parser Content
```Java
{
Name = dell-sw-mix-app-activity-assignedipaddress
  Vendor = Dell
  Product = Sonicwall
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"message":"""", """msg=\"Assigned IP address""", """ to MAC address """ ]
  Fields = [
    """time=\\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """"host":\{[^\}]*"name":"({host}[^\s"]+)""",
    """msg=\\"({event_name}[^"]+?)\\*"""",
    """Assigned IP address ({dest_ip}[A-Fa-f:\d.]+)""",
    """ to MAC address ({dest_mac}[A-Fa-f:\d.]+)""",
  ]


}
```