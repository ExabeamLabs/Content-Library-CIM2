#### Parser Content
```Java
{
Name = "cisco-asa-str-app-notification-updown"
  ParserVersion = "v1.0.0"
  Conditions = [ """%LINK-""", """UPDOWN:""" ]
  Fields = ${CiscoParsersTemplates.cisco-system-info.Fields} [
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