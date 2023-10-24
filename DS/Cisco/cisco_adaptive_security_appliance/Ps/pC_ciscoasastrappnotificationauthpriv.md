#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-authpriv
  ParserVersion = v1.0.0
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Conditions = [ """%AUTHPRIV-2-SYSTEM_MSG:""" ]

cisco-system-info = {
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SS","yyyy MMM dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SSS","epoch_sec"]
  Fields = [
     """({time}\d+ \w+ \d+ \d+:\d+:\d+)\s+\w+:\s+\%""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```