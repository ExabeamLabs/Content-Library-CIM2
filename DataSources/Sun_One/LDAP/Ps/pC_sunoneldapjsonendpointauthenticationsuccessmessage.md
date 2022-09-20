#### Parser Content
```Java
{
Name = sunone-ldap-json-endpoint-authentication-success-message
  Vendor = Sun One
  Product = LDAP
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"message":"A client attempted to access the server using SMB1."""" ]
  Fields = [
    """"@timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""",
    """"index":"[^\{\}]*?"host":"({host}[\w\-.]+)""",
    """"host":"({host}[\w\-.]+)"[^\{\}]*?"index":"""",
    """"destination":\{.*?"ipv4":"({dest_ip}[A-Fa-f:\d.]+)""",
    """"destination":\{.*?"host":"({dest_host}[\w\-.]+)""",
    """"source":\{.*?"ipv4":"({src_ip}[A-Fa-f:\d.]+)""",
    """"source":\{.*?"host":"({src_host}[\w\-.]+)""",
    """"message":"({event_name}[^"]+)""",
  ]



}
```