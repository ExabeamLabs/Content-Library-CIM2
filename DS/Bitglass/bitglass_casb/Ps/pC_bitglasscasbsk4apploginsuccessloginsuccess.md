#### Parser Content
```Java
{
Name = bitglass-casb-sk4-app-login-success-loginsuccess
  Vendor = Bitglass
  Product = Bitglass CASB
  TimeFormat = "dd MMM yyyy HH:mm:ss"
  Conditions = [ """api.bitglass.com""", """"ipaddress":""", """"email":""", """"dlppattern":""", """AutoProvision, User""" ]
  Fields = [
    """time=({time}\d+ \w+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """\ssuser=({email_address}[^@\s]+@({email_domain}[^\s@]+))""",
    """({operation}login-success)""",
    """({app}Bitglass)""",
    """"ipaddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"action":"({event_name}[^"]+)""",
    """"details":"({additional_info}[^"]+)""",
    """"device":"({os}[^"]+)""",
    """useragent":"({user_agent}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```