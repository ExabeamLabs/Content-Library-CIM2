#### Parser Content
```Java
{
Name = xiting-x-cef-app-login-success-erfolgreich
  Vendor = Xiting
  Product = XAMS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Login erfolgreich""", """CEF:""", """|Xiting|XAMS|""", """"USERID":"""" ]
  Fields = [
    """"USERID":"({user}[^"]+)"""",
    """({app}XAMS)""",
    """({event_name}Login erfolgreich)"""
    """"MSG":"({additional_info}[^"]+)""""
  ]


}
```