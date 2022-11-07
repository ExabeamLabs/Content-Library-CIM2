#### Parser Content
```Java
{
Name = cisco-secureendpoint-sk4-app-activity-orbital
  Vendor = Cisco
  Product = Cisco Secure Endpoint
  TimeFormat = "epoch_sec"
  Conditions = [  """"hostname":""", """destinationServiceName =Cisco AMP""", """"event_type":"Orbital """, """"orbital":""" ]
  Fields = [
    """"timestamp":({time}\d{10})""",
    """"event_type":"({event_name}[^"]+)""",
    """"hostname":"({host}[^"]+)""",
    """"external_ip":"({dest_ip}[a-fA-F:\d.]+)""",
    """"network_addresses":\[\{"ip":"({src_ip}[a-fA-F:\d.]+)""",
    """"group":"({url}[^"]+)""",
  ]
ParserVersion = "v1.0.0"


}
```