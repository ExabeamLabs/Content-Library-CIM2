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
    """USER:\s*({user}[\w\.\-]{1,40}\$?)""",
    """from\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\.?\s*$|\s\w+)""",
    """\s({event_name}logged in)""",
  ]


}
```