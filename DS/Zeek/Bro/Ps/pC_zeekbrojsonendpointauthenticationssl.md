#### Parser Content
```Java
{
Name = zeek-bro-json-endpoint-authentication-ssl
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Bro
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """"id.orig_h":""", """"id.resp_h":""", """"ssl",""" ]
  Fields = [
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid":"({connection_id}[^"]+)""",
    """"id\.orig_h":"({src_ip}[a-fA-F\d.:]+)""",
    """"id\.orig_p":({src_port}\d+)""",
    """"id\.resp_h":"({dest_ip}[a-fA-F\d.:]+)""",
    """"id\.resp_p":({dest_port}\d+)""",
    """"cipher":({auth_method}[^,]+)""",
    """"server_name":"({dest_host}[^"]+)""",
    """"validation_status":"({result}[^"]+)""",
    """"ja3":"({ja3}[^"]+)""",
# issuer is removed
  ]


}
```