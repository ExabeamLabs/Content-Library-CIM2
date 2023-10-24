#### Parser Content
```Java
{
Name = cisco-asa-str-app-activity-authmgr5
  ParserVersion = "v1.0.0"
  Conditions = [ """ %AUTHMGR-5-""" ]
  Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields}[
    """%AUTHMGR-5-({action}\w+):\s+({event_name}\S+\s+\S+)""",
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