#### Parser Content
```Java
{
Name = ibm-pnips-leef-app-activity-audit
  Vendor = IBM
  Product = Proventia Network IPS
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """LEEF:""", """|IBM|NIPS|""", """cat=Audit""" ]
  Fields = [
    """devTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """LEEF:([^\|]*\|){4}({event_name}[^\|]+)""",
    """cat=({event_category}[^=\|\#]+)""",
    """proto=({protocol}[^\=\|\#]+)""",
    """sev=({alert_severity}[^\=\|\#]+)""",
    """src=({src_ip}[A-Fa-f:\d.]+)""",
    """dst=({dest_ip}[A-Fa-f:\d.]+)""",
    """srcPort=({src_port}\d+)""",
    """dstPort=({dest_port}\d+)""",
    """status=({action}[^\=\|\#]+)""",
# adapter_id is removed
  ]


}
```