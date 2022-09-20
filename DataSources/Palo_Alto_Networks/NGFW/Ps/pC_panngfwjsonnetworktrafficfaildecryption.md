#### Parser Content
```Java
{
Name = pan-ngfw-json-network-traffic-fail-decryption
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"source":"Palo Alto Networks FLS LF"""", """"LogType":"DECRYPTION"""", """"SubType":"start"""", """"FromZone":"""", """"ToZone":"""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"host":"({host}[^"]+)"""",
    """"SourceUser":"({email_address}[^"@]+@[^"]+)"""",
    """"SourceAddress":"({src_ip}[a-fA-F\d:.]+)"""",
    """"DestinationAddress":({dest_ip}[a-fA-F\d:.]+)"""",
    """"SourcePort":({src_port}\d+)""",
    """"DestinationPort":({dest_port}\d+)""",
    """"NATSource":"({src_translated_ip}[a-fA-F\d:.]+)"""",
    """"NATDestination":"({dest_translated_ip}[a-fA-F\d:.]+)"""",
    """"NATSourcePort":({src_translated_port}\d+)""",
    """"NATDestinationPort":({dest_translated_port}\d+)""",
    """"LogType":"({event_name}[^"]+)"""",
    """"SubType:"({operation}[^"]+)"""",
    """"Action":"({action}[^"]+)"""",
    """"Protocol":"({protocol}[^"]+)"""",
    """"Rule":"({rule}[^"]+)"""",
    """"PolicyName":"({additional_info}[^"]+)"""",
    """"FromZone":"({src_network_zone}[^"]+)"""",
    """"ToZone":"({dest_network_zone}[^"]+)""""
  ]


}
```