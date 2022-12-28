#### Parser Content
```Java
{
Name = pan-ngfw-json-vpn-logout-success-logout
  Conditions = [ """"LogType":"USERID"""", """"DeviceSN":"""", """"Subtype":"logout"""", """"MappingDataSourceType":"globalprotect"""" ]
  Fields = ${PaloAltoParsersTemplates.paloalto-vpn.Fields}[
    """"SourceIP":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
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
    """"PrivateIPv(4|6)":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"PublicIPv(4|6)":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"Source(Address|IP)":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"DestinationAddress":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"(Source)?User(Name)?":"((na|NA|({domain}[^"\\]+))\\+)?(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[^"]+))"""",
    """"SourcePort":({src_port}\d+)""",
    """"DestinationPort":({dest_port}\d+)""",
    """"Protocol":"({protocol}[^"]+)"""",
    """"LogType":"({event_category}[^"]+)""""
  
}
```