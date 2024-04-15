#### Parser Content
```Java
{
Name = "zeek-zeek-json-certificate-exchange-certificate"
  Vendor = "Zeek"
  Product = "Zeek"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [  """certificate.issuer":""", """"certificate.subject":""", """"certificate.key_alg":"""]
  Fields = [
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"id":"({file_id}[^"]+)""",
    """"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"id\.orig_p":({src_port}\d+)""",
    """"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"id\.resp_p":({dest_port}\d+)""",
    """"certificate\.version":"({version}[^"]+)""",
# serial is removed
    """"command":"({operation}[^"]+)""",
# issuer is removed
    """"certificate\.subject":"CU=({client_cert_subject}[^,]+)""",
# algorithm is removed
  ]


}
```