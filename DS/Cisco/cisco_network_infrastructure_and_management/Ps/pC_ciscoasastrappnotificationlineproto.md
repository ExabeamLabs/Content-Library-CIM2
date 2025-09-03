#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-lineproto
  ParserVersion = v1.0.0
  Conditions = [ """%LINEPROTO-""", """UPDOWN:""" ]
  Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
    """({event_code}%LINEPROTO-[^:]+)""",
    """\-UPDOWN:\s*({event_name}[^:=]+?)(\s\w+[:=.]|\s*$)"""
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d.\d\d\d)"""
  ]

cisco-system-info = {
  Vendor = Cisco
  Product = Cisco Network Infrastructure and Management
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss", "MMM dd yyyy HH:mm:ss.SSS", "yyyy MMM dd HH:mm:ss", "yyyy MMM dd HH:mm:ss.SSSSSS"]
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