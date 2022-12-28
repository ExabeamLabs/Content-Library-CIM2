#### Parser Content
```Java
{
Name = oracle-pc-sk4-network-traffic-success-dataevent
Vendor = "Oracle"
Product = "Oracle Public Cloud"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  ""","type":"com.oraclecloud.vcn.flowlogs.DataEvent""""
  ""","flowid":""""
  ""","oracle":{""""
  """"compartmentid":""""
]
Fields = [
  """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""""
  """"sourceAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"sourcePort":({src_port}\d+)"""
  """"destinationAddress":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """"destinationPort":({dest_port}\d+)"""
  """"action":"({result}[^"]+)""""
  """"bytesOut":({bytes_out}\d+)"""
  """"protocolName":"({protocol}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```