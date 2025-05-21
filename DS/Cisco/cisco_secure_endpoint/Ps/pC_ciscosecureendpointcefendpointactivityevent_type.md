#### Parser Content
```Java
{
Name = cisco-secureendpoint-cef-endpoint-activity-event_type
  Vendor = "Cisco"
  Product = Cisco Secure Endpoint
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"event_type":""", """"links":{""", """"trajectory":""", """"timestamp_nanoseconds":""", """cisco""" ]
  Fields = [
    """"timestamp":\s*({time}\d{10})""",
    """"hostname":"({src_host}[\w\.\-]+)"""",
    """"external_ip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"network_addresses":.+?"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
 	""""mac":\s*"({src_mac}[^"]+)"""",
 	""""event_type":\s*"({event_name}[^"]+)""",
 	""""connector_guid":"({connector_guid}[^"]+)"""",
    """"links":\{({more_info}[^\}]+)\}""",
    """"trajectory":\s*"({additional_info}[^"]+)""",
    """"ecx":"({failure_reason}[^"]+)"""",
    """"error_code":({error_code}\d+)""",
    """"group":"({url}[^"]+)"""
  ]


}
```