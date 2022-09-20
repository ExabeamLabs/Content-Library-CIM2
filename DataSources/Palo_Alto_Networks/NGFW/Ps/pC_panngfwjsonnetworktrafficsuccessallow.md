#### Parser Content
```Java
{
Name = pan-ngfw-json-network-traffic-success-allow
  ParserVersion = v1.0.0
  Conditions = [ """"LogType":"TRAFFIC"""", """"Action":"allow"""", """"Subtype":"""" ]
  Fields = ${PaloAltoParsersTemplates.paloalto-vpn.Fields}[
    """"Action":"({action}[^"]+)"""",
    """"NATSource":"({src_translated_ip}[a-fA-F\d:.]+)""",
    """"NATDestination":"({dest_translated_ip}[a-fA-F\d:.]+)""",
    """"NATSourcePort":({src_translated_port}\d+)""",
    """"NATDestinationPort":({src_translated_port}\d+)""",
    """"Bytes":({bytes}\d+),""",
    """"BytesSent":({bytes_out}\d+),""",
    """"BytesReceived":({bytes_in}\d+),""",
    """"URLCategory":"({category}[^"]+)"""",
    """"Application":"({network_app}[^"]+)"""",
    """"FromZone":"({src_network_zone}[^"]+)"""",
    """"ToZone":"({dest_network_zone}[^"]+)""""
  ]

paloalto-vpn = {
  Vendor = Palo Alto Networks
  Product = NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)""",
    """"host":"({host}[^"]+)"""",
    """"DeviceName":"({host}[^"\s]+)"""",
    """"PrivateIPv(4|6)":"({src_ip}[a-fA-F\d:.]+)""",
    """"PublicIPv(4|6)":"({dest_ip}[a-fA-F\d.:]+)""",
    """"Source(Address|IP)":"({src_ip}[a-fA-F\d:.]+)""",
    """"DestinationAddress":"({dest_ip}[a-fA-F\d:.]+)""",
    """"(Source)?User(Name)?":"((na|NA|({domain}[^"\\]+))\\+)?(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[^"]+))"""",
    """"SourcePort":({src_port}\d+)""",
    """"DestinationPort":({dest_port}\d+)""",
    """"Protocol":"({protocol}[^"]+)"""",
    """"LogType":"({event_category}[^"]+)""""
  
}
```