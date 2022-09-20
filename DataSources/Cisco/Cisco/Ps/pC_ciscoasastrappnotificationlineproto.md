#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-lineproto
  ParserVersion = v1.0.0
  Product = Cisco
  Conditions = [ """%LINEPROTO-""", """UPDOWN:""" ]
  Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
    """({event_code}%LINEPROTO-[^:]+)""",
    """\-UPDOWN:\s*({event_name}[^:=]+?)(\s\w+[:=.]|\s*$)"""
  ]

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