#### Parser Content
```Java
{
Name = cisco-ios-str-app-notification-success-isis
  ParserVersion = v1.0.0
  Product = Cisco IOS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ISIS""", """%CLNS""" ]
  Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
    """({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s(pdt|PDT):"""
    """({protocol}ISIS)"""
    """({event_code}%[\s\w+-]+):[^:]+:\s*({event_name}.+)"""
  ]

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