#### Parser Content
```Java
{
Name = pan-ngfw-json-network-traffic-start-1
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [  """"LogType":"DECRYPTION"""", """"Subtype":"start"""", """"FromZone":"""", """"ToZone":"""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"host":"({host}[^"]+)"""",
    """"SourceUser":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"SourceAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"DestinationAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"SourcePort":({src_port}\d+)""",
    """"DestinationPort":({dest_port}\d+)""",
    """"NATSource":"({src_translated_ip}[a-fA-F\d:.]+)"""",
    """"NATDestination":"({dest_translated_ip}[a-fA-F\d:.]+)"""",
    """"NATSourcePort":({src_translated_port}\d+)""",
    """"NATDestinationPort":({dest_translated_port}\d+)""",
    """"LogType":"({event_name}[^"]+)"""",
    """"Subtype":"({operation}[^"]+)"""",
    """"Action":"({result}[^"]+)"""",
    """"Protocol":"({protocol}[^"]+)"""",
    """"Rule":"({rule}[^"]+)"""",
    """"PolicyName":"({additional_info}[^"]+)"""",
    """"FromZone":"({src_network_zone}[^"]+)"""",
    """"ToZone":"({dest_network_zone}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```