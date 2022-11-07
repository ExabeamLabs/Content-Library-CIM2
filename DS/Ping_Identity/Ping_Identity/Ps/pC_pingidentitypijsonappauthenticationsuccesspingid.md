#### Parser Content
```Java
{
Name = pingidentity-pi-json-app-authentication-success-pingid
  Vendor = Ping Identity
  Product = Ping Identity
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""source": "PINGID"""",""""type": "user"""",""""status": "SUCCESS"""",""""message":""",""""resources":""",""""client":"""]
  Fields = [
    """"recorded":\s+"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """"name":\s"(({email_address}[^"@\s]+@[^"]+)|({user}[^"]+))"""",
    """"status":\s*"({result}SUCCESS)""",
    """"message":\s+"({additional_info}[^}]+?)"\s*\}""",
    """sourceip="({src_ip}[A-Fa-f\d.:]+)""""
  ]


}
```