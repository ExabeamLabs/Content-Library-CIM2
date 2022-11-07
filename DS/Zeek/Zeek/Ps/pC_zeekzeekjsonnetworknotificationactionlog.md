#### Parser Content
```Java
{
Name = zeek-zeek-json-network-notification-actionlog
  Vendor = Zeek
  Product = Zeek
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = ["""Notice::ACTION_LOG"""]
  Fields = [
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid":"({connection_id}[^"]+)""",
    """"id\.orig_h":"({src_ip}[a-fA-F\d.:]+)""",
    """"id\.orig_p":({src_port}\d+)""",
    """"id\.resp_h":"({dest_ip}[a-fA-F\d.:]+)""",
    """"id\.resp_p":({dest_port}\d+)""",
    """"proto":"({protocol}[^"]+)""",
    """"msg":"({additional_info}[^"]+)""",
# peer is removed
    """"sub":"({user}[^"]+)""",
  ]


}
```