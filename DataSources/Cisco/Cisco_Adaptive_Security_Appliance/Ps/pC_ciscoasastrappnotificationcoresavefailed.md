#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-coresavefailed
  ParserVersion = v1.0.0
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Conditions = [ """%SYSMGR-2-CORE_SAVE_FAILED:""" ]

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