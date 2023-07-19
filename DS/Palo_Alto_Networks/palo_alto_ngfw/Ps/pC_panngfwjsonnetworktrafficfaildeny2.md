#### Parser Content
```Java
{
Name = pan-ngfw-json-network-traffic-fail-deny-2
  Conditions = [ """"LogType":"TRAFFIC"""", """"Subtype":"end"""", """"Action":"drop-reset"""" ]
  Fields = ${PaloAltoParsersTemplates.paloalto-vpn.Fields}[
    """"Action":"({result}[^"]+)"""",
    """"NATSource":"({src_translated_ip}[a-fA-F\d:.]+)""",
    """"NATDestination":"({dest_translated_ip}[a-fA-F\d:.]+)""",
    """"NATSourcePort":({src_translated_port}\d+)""",
    """"NATDestinationPort":({dest_translated_port}\d+)""",
    """"Bytes":({bytes}\d+),""",
    """"BytesSent":({bytes_out}\d+),""",
    """"BytesReceived":({bytes_in}\d+),""",
    """"URLCategory":"({category}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"

paloalto-vpn = {
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)""",
    """"host":"({host}[^"]+)"""",
    """"DeviceName":"({host}[^"\s]+)"""",
    """"PrivateIPv(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"PublicIPv(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"Source(Address|IP)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"DestinationAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"(Source)?User(Name)?":"((na|NA|({domain}[^"\\]+))\\+)?(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[^"]+))"""",
    """"SourcePort":({src_port}\d+)""",
    """"DestinationPort":({dest_port}\d+)""",
    """"Protocol":"({protocol}[^"]+)"""",
    """"LogType":"({event_category}[^"]+)"""",
    """"AuthMethod":"({auth_method}[^"]+)"""",
    """"EventIDValue":"({event_name}[^"]+)"""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  
}
```