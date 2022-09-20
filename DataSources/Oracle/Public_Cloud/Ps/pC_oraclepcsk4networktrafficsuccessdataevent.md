#### Parser Content
```Java
{
Name = oracle-pc-sk4-network-traffic-success-dataevent
Vendor = "Oracle"
Product = "Public Cloud"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  ""","type":"com.oraclecloud.vcn.flowlogs.DataEvent""""
  ""","flowid":""""
  ""","oracle":{""""
  """"compartmentid":""""
]
Fields = [
  """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""""
  """"sourceAddress":"({src_ip}[a-fA-F\d:\.]+)""""
  """"sourcePort":({src_port}\d+)"""
  """"destinationAddress":"({dest_ip}[a-fA-F\d:\.]+)""""
  """"destinationPort":({dest_port}\d+)"""
  """"action":"({result}[^"]+)""""
  """"bytesOut":({bytes_out}\d+)"""
  """"protocolName":"({protocol}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```