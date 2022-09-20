#### Parser Content
```Java
{
Name = bitglass-casb-sk4-app-login-success-loginsuccess
  Vendor = Bitglass
  Product = Bitglass CASB
  TimeFormat = "dd MMM yyyy HH:mm:ss"
  Conditions = [ """|login-success|""","""destinationServiceName =Bitglass""",""" cs6=""" ]
  Fields = [
    """time=({time}\d+ \w+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """\ssuser=({email_address}[^@\s]+@({email_domain}[^\s@]+))""",
    """({operation}login-success)""",
    """({app}Bitglass)""",
    """"ipaddress":"({src_ip}[\da-fA-F.:]+)"""",
    """"action":"({event_name}[^"]+)""",
    """"details":"({additional_info}[^"]+)""",
    """"device":"({os}[^"]+)""",
    """useragent":"({user_agent}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```