#### Parser Content
```Java
{
Name = "helpsystems-powertechiam-kv-endpoint-login-success-loginok"
  Vendor = "HelpSystems"
  Product = "Powertech Identity and Access Manager"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """login - login_ok"""
    """Successful login"""
  ]
  Fields = [
    """clientTime=\"*({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)Z\"*"""
    """authHost=\"*({dest_host}({host}[^\"]+))\""""
    """user=\"*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
  ]
  ParserVersion = "v1.0.0"


}
```