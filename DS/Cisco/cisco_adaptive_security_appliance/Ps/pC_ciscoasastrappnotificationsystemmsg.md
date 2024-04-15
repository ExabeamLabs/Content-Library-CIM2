#### Parser Content
```Java
{
Name = "cisco-asa-str-app-notification-systemmsg"
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """%DAEMON-2-SYSTEM_MSG:""" ]

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