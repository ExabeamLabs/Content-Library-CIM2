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
  
}
```