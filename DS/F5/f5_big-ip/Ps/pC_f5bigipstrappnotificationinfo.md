#### Parser Content
```Java
{
Name = f5-bigip-str-app-notification-info
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 BIG-IP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ notice icrd_child: """, """INFO""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s\w+""",
    """icrd_child:\s+({event_code}\d+)""",
    """,\s+INFO,({additional_info}[^,]+?)\s*$""",
    """({event_category}RestRequestSender)"""
  ]


}
```