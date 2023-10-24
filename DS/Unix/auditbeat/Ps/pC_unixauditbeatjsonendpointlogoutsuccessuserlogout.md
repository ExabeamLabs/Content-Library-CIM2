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
    """"hostname":"({host}[\w\-.]+?)(@[^"]*)?""""
    """"user":\{.+?name":"({user}[\w\.\-]{1,40}\$?)"""",
    """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"action":"({event_name}[^"]+)"""",
    """"message":"({additional_info}[^"]+)"""",
    """"domain":"({domain}[^"]+)""""
  ]
  DupFields = ["host->dest_host"]


}
```