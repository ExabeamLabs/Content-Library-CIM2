#### Parser Content
```Java
{
Name = cisco-ios-str-app-notification-success-isis
  ParserVersion = v1.0.0
  Product = Cisco IOS
  Conditions = [ """ISIS""", """%CLNS""" ]
  Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
    """(({time}\w+ \d+ \d+:\d+:\d+)\s)?({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s(pdt|PDT):"""
    """({protocol}ISIS)"""
    """({event_code}%[\s\w+-]+):[^:]+:\s*({event_name}.+)"""
  ]

cisco-system-info = {
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SS","yyyy MMM dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SSS","epoch_sec","epoch", "MMM dd HH:mm:ss"]
  Fields = [
    """\s({time}\w+ \d+ \d+:\d+:\d+)"""
     """({time}\d+ \w+ \d+ \d+:\d+:\d+)\s+\w+:\s+\%""",
     """\Wrt=({time}\d{13})""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```