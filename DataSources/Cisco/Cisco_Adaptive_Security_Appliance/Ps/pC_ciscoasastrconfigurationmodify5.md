#### Parser Content
```Java
{
Name = cisco-asa-str-configuration-modify-5
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Conditions = [ """%VSHD-5-VSHD_SYSLOG_CONFIG_I:""" ]

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