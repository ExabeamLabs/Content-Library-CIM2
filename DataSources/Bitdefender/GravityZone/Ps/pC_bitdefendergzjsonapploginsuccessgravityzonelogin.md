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
    """"user_name":"(({email_address}({user}[^"@\\\/\s]+)@({domain}[^.]+)[^"]+))""",
    """"os":"({os}[^"]+)""",
    """"browser_name":"({browser}[^"]+)""",
    """"device_ip":"({src_ip}[A-Fa-f:\d.]+)""",
  ]
  DupFields = ["domain->email_domain"]


}
```