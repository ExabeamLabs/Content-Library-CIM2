#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-cslu
    ParserVersion = v1.0.0
    Conditions = [ """%LICMGR-3-LOG_SMART_LIC_COMM_FAILED:""" ]
    Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
      """host:\s*({host}[\w\-.]+)"""
      """pid=({process_id}\d+)"""
      """\s*({time}\w+ \d+ \d+:\d+:\d+)"""
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