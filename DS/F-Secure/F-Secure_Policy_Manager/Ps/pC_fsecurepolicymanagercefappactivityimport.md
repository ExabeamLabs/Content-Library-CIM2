#### Parser Content
```Java
{
Name = fsecure-policymanager-cef-app-activity-import
  ParserVersion = "v1.0.0"
  Vendor = F-Secure
  Product = F-Secure Policy Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CEF:""", """|F-Secure|F-Secure Policy Manager|""" ]
  Fields = [
    """({host}[\w.\-]+) CEF:([^\|]*\|){5}({event_name}[^\|]+)""",
    """\Wshost=(|({src_host}.+?))(\s+\w+=|\s*$)""",
    """\Wmsg=(|({additional_info}.+?))(\s+\w+=|\s*$)""",
  ]


}
```