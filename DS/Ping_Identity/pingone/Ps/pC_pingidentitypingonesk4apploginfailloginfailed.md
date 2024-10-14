#### Parser Content
```Java
{
Name = pingidentity-pingone-sk4-app-login-fail-loginfailed
  Vendor = Ping Identity
  Product = PingOne
  TimeFormat = "epoch"
  Conditions = [ """destinationServiceName =Ping""", """|login-failed|""" ]
  Fields = [
    """end=({time}\d{13})""",
    """cat=({category}[^\s]+)"""
    """request=({result}[^\s]+)""",
    """requestClientApplication=({app}.*?)\s\w+=""",
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """flexString2=({auth_method}.*?)\s\w+=""",
    """message":"({auth_method}[^\\]+)\s\\"({device_name}[^\\]+)""",
    """msg=({result_reason}.*?)\s\w+=""",
  ]
  ParserVersion = "v1.0.0"


}
```