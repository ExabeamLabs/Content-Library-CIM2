#### Parser Content
```Java
{
Name = pan-ngfw-json-vpn-logout-success-logout
  Conditions = [ """"LogType":"USERID"""", """"DeviceSN":"""", """"Subtype":"logout"""", """"MappingDataSourceType":"globalprotect"""" ]
  Fields = ${PaloAltoParsersTemplates.paloalto-vpn.Fields}[
    """"SourceIP":"({src_ip}[A-Fa-f\d\.:]+)""""
  ]
  ParserVersion = "v1.0.0"

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