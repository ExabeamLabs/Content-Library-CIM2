#### Parser Content
```Java
{
Name = pan-ngfw-json-network-traffic-fail-actiondrop
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"LogType":"TRAFFIC"""", """"Action":"drop"""", """"Subtype":"drop"""", """"Rule":"""" ]
  Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)"""
  """"host":"({host}[\w\-.]+)"""
  """"DeviceName":"({host}[\w\-.]+)"""
  """"SourceAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"DestinationAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """"SourcePort":({src_port}\d{1,5})"""
  """"DestinationPort":({dest_port}\d{1,5})"""
  """"LogType":"({event_category}[^"]+)""""
  """"Protocol":"({protocol}[^"]+)""""
  """"Action":"({action}[^"]+)""""
  """"Bytes":({bytes}\d+),"""
  """"BytesSent":({bytes_out}\d+),"""
  """"BytesReceived":({bytes_in}\d+),"""
  """"URLCategory":"({category}[^"]+)""""  
  ]


}
```