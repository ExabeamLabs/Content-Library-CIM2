#### Parser Content
```Java
{
Name = xiting-x-cef-app-login-fail-gescheitert
  Vendor = Xiting
  Product = XAMS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Login gescheitert""", """CEF:""", """|Xiting|XAMS|""", """"USERID":"""" ]
  Fields = [
    """"USERID":"({user}[^"]+)"""",
    """({app}XAMS)""",
    """({event_name}Login gescheitert)"""
    """"MSG":"({additional_info}[^"]+)""""
  ]  


}
```