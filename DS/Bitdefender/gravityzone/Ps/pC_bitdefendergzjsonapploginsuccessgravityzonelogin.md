#### Parser Content
```Java
{
Name = bitdefender-gz-json-app-login-success-gravityzonelogin
  ParserVersion = v1.0.0
  Vendor = Bitdefender
  Product = GravityZone
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """gravityzone:""", """"name":"Login from new device"""" ]
  Fields = [
    """"created":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({app}gravityzone)""",
    """"name":"({operation}[^"]+)""",
    """"user_name":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"os":"({os}[^"]+)""",
    """"browser_name":"({browser}[^"]+)""",
    """"device_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]


}
```