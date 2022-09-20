#### Parser Content
```Java
{
Name = zeek-z-json-network-traffic-name
  Vendor = Zeek
  Product = Zeek
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [  """notice":""", """"name":"""]
  Fields = [
    """"_system_name":"({host}[^"]+)""",
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid":"({user_uid}[^"]+)""",
    """"id\.orig_h":"({src_ip}[a-fA-F\d.:]+)""",
    """"id\.orig_p":({src_port}\d+)""",
    """"id\.resp_h":"({dest_ip}[a-fA-F\d.:]+)""",
    """"id\.resp_p":({dest_port}\d+)""",
    """"name":"({event_name}[^"]+)""",
# notice is removed
# peer is removed
  ]


}
```