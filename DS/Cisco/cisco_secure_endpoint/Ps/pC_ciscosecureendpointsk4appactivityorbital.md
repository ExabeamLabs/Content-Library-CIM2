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
    """"external_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"network_addresses":\[\{"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"group":"({url}[^"]+)""",
  ]
ParserVersion = "v1.0.0"


}
```