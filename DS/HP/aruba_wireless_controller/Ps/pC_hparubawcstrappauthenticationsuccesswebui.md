#### Parser Content
```Java
{
Name = hp-arubawc-str-app-authentication-success-webui
  Vendor = HP
  Product = Aruba Wireless controller
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """webui""", """ USER: """,""" has logged in from """ ]
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d\:\d\d\s\d\d\d\d)\s({host}[^\s]+)""",
    """USER:\s*({user}[^\s\@]+)""",
    """from\s({src_ip}[a-fA-F\d:\.]+?)(\.?\s*$|\s\w+)""",
    """\s({event_name}logged in)""",
  ]


}
```