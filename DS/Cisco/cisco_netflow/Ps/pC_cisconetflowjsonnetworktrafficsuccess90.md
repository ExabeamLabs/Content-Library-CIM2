#### Parser Content
```Java
{
Name = cisco-netflow-json-network-traffic-success-90
Vendor = "Cisco"
Product = "Cisco Netflow"
TimeFormat = "yyyy-MMM-dd HH:mm:ss"
flow_start_timeFormat = ["epoch_sec"]
flow_end_timeFormat = ["epoch_sec"]
Conditions = [
  """"bytes_in":"""
  """"exporter_time":""""
  """"packets_in":"""
  """"tcp_flags":"""
  """"flow_start_time":"""
]
Fields = [
  """"exporter_time":"({time}\d+-\w+-\d+\s+\d+:\d+:\d+)"""
  """"bytes_in":({bytes_in}\d+)"""
  """"bytes_out":({bytes_out}\d+)"""
  """"dest_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"dest_port":({dest_port}\d+)"""
  """"flow_end_time":({flow_end_time}\d{10})"""
  """"flow_start_time":({flow_start_time}\d{10})"""
  """"packets_in":({packets_in}\d+)"""
  """"packets_out":({packets_out}\d+)"""
  """"protoid":({protocol}\d+)"""
  """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"src_port":({src_port}\d+)"""
  """"tcp_flags":({tcp_flags}\d+)"""
]
DupFields = [
  "bytes_in->bytes"
  "packets_in->packets"]
ParserVersion = "v1.0.0"


}
```