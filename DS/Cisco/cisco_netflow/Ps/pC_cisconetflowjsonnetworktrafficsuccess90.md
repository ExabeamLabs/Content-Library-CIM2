#### Parser Content
```Java
{
Name = cisco-netflow-json-network-traffic-success-90
Vendor = "Cisco"
Product = "Cisco Netflow"
ExtractionType = json
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
  """exa_json_path=$.exporter_time,exa_field_name=time"""
  """exa_json_path=$.bytes_in,exa_field_name=bytes_in"""
  """exa_json_path=$.bytes_out,exa_field_name=bytes_out"""
  """exa_json_path=$.dest_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """exa_json_path=$.dest_port,exa_field_name=dest_port"""
  """exa_json_path=$.flow_end_time,exa_field_name=flow_end_time"""
  """exa_json_path=$.flow_start_time,exa_field_name=flow_start_time"""
  """exa_json_path=$.packets_in,exa_field_name=packets_in"""
  """exa_json_path=$.packets_out,exa_field_name=packets_out"""
  """exa_json_path=$.protoid,exa_field_name=protocol"""
  """exa_json_path=$.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.src_port,exa_field_name=src_port"""
  """exa_json_path=$.tcp_flags,exa_field_name=tcp_flags"""
]
DupFields = [
  "bytes_in->bytes"
  "packets_in->packets"]
ParserVersion = "v1.0.0"


}
```