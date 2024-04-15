#### Parser Content
```Java
{
Name = "cisco-asa-str-app-notification-startstop"
  ParserVersion = "v1.0.0"
  Conditions = [ """%SYS-""", """LOGGINGHOST_STARTSTOP:""" ]
  Fields = ${CiscoParsersTemplates.cisco-system-info.Fields} [
    """LOGGINGHOST_STARTSTOP:\s*Logging to host ({host}[A-Fa-f:\d.]+) port ({dest_port}\d+)""",
  ]

cisco-system-info = {
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
     """({time}\d+ \w+ \d+ \d+:\d+:\d+)\s+\w+:\s+\%""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```