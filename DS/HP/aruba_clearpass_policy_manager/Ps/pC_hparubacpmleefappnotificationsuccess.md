#### Parser Content
```Java
{
Name = hp-arubacpm-leef-app-notification-success
  Vendor = "HP"
  Product = Aruba ClearPass Policy Manager
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Conditions = [ """LEEF:""", """|Aruba Networks|ClearPass|""", """action=""", """cat=System Events""", """description=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+LEEF:""",
    """devTime=({time}[^=]+?)\s+\w+?=""",
    """action=(None|({action}[^=]+?))\s+\w+?=""",
    """description=({operation}[^=]+?)\.""",
    """device=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """description=({event_name}[^=]+?)\.""",
  ]


}
```