#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-coresavefailed
  ParserVersion = v1.0.0
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Conditions = [ """%SYSMGR-2-CORE_SAVE_FAILED:""" ]

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
    """({event_code}%\w+\-[^:\s]+):""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  cisco-system-info = {
  Vendor = Cisco
  Product = Cisco Network Infrastructure and Management
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss", "MMM dd yyyy HH:mm:ss.SSS", "yyyy MMM dd HH:mm:ss", "yyyy MMM dd HH:mm:ss.SSSSSS", "MMM dd HH:mm:ss.SSS", "MMM  d HH:mm:ss.SSS"]
  Fields = [
    """(\d+|({host}[\w\-\.]+))\s*:\s*(\d+\s)?\w+\s\d+\s\d\d:\d\d:\d\d""",
    """\s({time}\w+ \d+ \d+:\d+:\d+)""",
    """({time}\d+ \w+ \d+ \d+:\d+:\d+(\.\d{6})?)\s+\w+:\s+\%\w+-""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$""",
    """\sinterface\s({interface}\w+\/\d+)(,|\s)""",
    """:\s*%\w+\-({priority}\d+)-({event_name}[^:]+)\s*:"""
  ]
}
}
```