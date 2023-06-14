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
    """Assigned IP address ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """ to MAC address ({dest_mac}[A-Fa-f:\d.]+)""",
    """\spri=({alert_severity}\d+)""",
    """\sfw=({firewall}[a-fA-F\d.:]+)""",
    """\sm=({message_id}\d+)""",
    """\smsg="({alert_name}[^:"-]+?)\s*(:|"|-)"""
    """\smsg="({additional_info}[^"]+?)\s*"""",
    """\sc=({category_id}\d+)"""
  ]
  DupFields = [ "message_id->alert_type" ]


}
```