#### Parser Content
```Java
{
Name = unix-auditbeat-json-endpoint-logout-success-userlogout
  Vendor = Unix
  Product = Auditbeat
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""auditbeat"""",""""action":"user_logout"""",""""category":["authentication"""]
  Fields = [
    """timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""",
    """"hostname":"({host}[^"]+)""""
    """"user":\{.+?name":"({user}[^"]+)"""",
    """"ip":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
    """"action":"({event_name}[^"]+)"""",
    """"message":"({additional_info}[^"]+)"""",
    """"domain":"({domain}[^"]+)""""
  ]
  DupFields = ["host->dest_host"]


}
```