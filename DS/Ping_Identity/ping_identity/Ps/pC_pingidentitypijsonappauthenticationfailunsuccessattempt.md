#### Parser Content
```Java
{
Name = pingidentity-pi-json-app-authentication-fail-unsuccessattempt
  Vendor = Ping Identity
  Product = Ping Identity
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"source":"PINGID"""", """"type":"user"""", """"status":"UNSUCCESSFUL_ATTEMPT"""",""""message":""",""""resources":""",""""result":{"""]
  Fields = [
    """"recorded":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """"name":"({user}[^"]+)"""",
    """"status":"({result}[^"]+)"""",
    """"message":"({additional_info}[^}]+?)"\s*\}"""
  ]


}
```