#### Parser Content
```Java
{
Name = pan-ngfw-json-network-traffic-start
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"LogSetting":"CDL"""", """"LogType":"DECRYPTION"""", """"SubType":"start"""", """"FromZone":"""", """"ToZone":"""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"host":"({host}[^"]+)"""",
    """"SourceUser":"({email_address}[^"@]+@[^"]+)"""",
    """"SourceAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"DestinationAddress":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"SourcePort":({src_port}\d+)""",
    """"DestinationPort":({dest_port}\d+)""",
    """"NATSource":"({src_translated_ip}[a-fA-F\d:.]+)"""",
    """"NATDestination":"({dest_translated_ip}[a-fA-F\d:.]+)"""",
    """"NATSourcePort":({src_translated_port}\d+)""",
    """"NATDestinationPort":({dest_translated_port}\d+)""",
    """"LogType":"({event_name}[^"]+)"""",
    """"SubType":"({operation}[^"]+)"""",
    """"Action":"({action}[^"]+)"""",
    """"Protocol":"({protocol}[^"]+)"""",
    """"Rule":"({rule}[^"]+)"""",
    """"PolicyName":"({additional_info}[^"]+)"""",
    """"FromZone":"({src_network_zone}[^"]+)"""",
    """"ToZone":"({dest_network_zone}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```