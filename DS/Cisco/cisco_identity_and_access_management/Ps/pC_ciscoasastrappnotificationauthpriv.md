#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-authpriv
  ParserVersion = v1.0.0
  Product = Cisco Identity and Access Management
  Conditions = [ """%AUTHPRIV-2-SYSTEM_MSG:""" ]

cisco-system-info-aa = {
  Vendor = "Cisco"
  Product = Cisco Network Infrastructure and Management
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SS","yyyy MMM dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SSS","epoch_sec","epoch", "MMM dd HH:mm:ss", "MMM dd HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy MMM dd HH:mm:ss.SSSSSS"]
  Fields = [
    """(\d+:\s*({host}[\w\-\.]+)\s*(:\s*\d+)?:\s*)?\w+\s\d+\s(\d\d\d\d\s)?\d\d:\d\d:\d\d(\.\d+)?(\s\w+)?:\s*%"""
    """\w+\s\d+\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)\s"""
    """\s({time}\w+ \d+(\s*\d+)? \d+:\d+:\d+(\.\d+)?)"""
    """({time}\d+ \w+ \d+ \d+:\d+:\d+(\.\d+)?)\s+\w+:\s+\%""",
    """\Wrt=({time}\d{13})""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```