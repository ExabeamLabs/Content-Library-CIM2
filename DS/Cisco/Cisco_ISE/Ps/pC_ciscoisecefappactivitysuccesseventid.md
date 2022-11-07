#### Parser Content
```Java
{
Name = cisco-ise-cef-app-activity-success-eventid
  Vendor = Cisco
  Product = Cisco ISE
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [  """|Cisco|Cisco ISE|""", """CEF:""", """msg=""", """eventId=""" ]
  Fields = [
    """\Wrt=({time}\d+)""",
    """shost=({src_host}[^\s]+)""",
    """Cisco ISE\|(|[^\|]+)\|(|[^\|]+)\|({event_name}[^\|]+)""",
    """suser=({user}[^\s]+)""",
    """dhost=({dest_host}[^\s]+)""",
    """dst=({dest_ip}[A-Fa-f:\d.]+)""",
    """dpt=({dest_port}\d+)""",
    """Cisco ISE\|*({event_code}\d+)\|""",
    """cat=({category}[^\s]+)\s""",
    """deviceSeverity=({severity}[^\s]+)""",
    """cs1=({auth_method}[^\s]+)""",
  ]


}
```