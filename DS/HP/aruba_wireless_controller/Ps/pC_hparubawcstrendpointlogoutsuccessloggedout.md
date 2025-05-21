#### Parser Content
```Java
{
Name = hp-arubawc-str-endpoint-logout-success-loggedout
  ParserVersion = "v1.0.0"
  Vendor = HP
  Product = Aruba Wireless controller
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """fpcli:""", """ USER: """, """connected from """,""" has logged out""" ]
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d\:\d\d\s\d\d\d\d)\s({host}[^\s]+)""",
    """USER:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """from\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\.\s$|\s\w+)""",
    """\s({event_name}logged out)""",
  ]


}
```