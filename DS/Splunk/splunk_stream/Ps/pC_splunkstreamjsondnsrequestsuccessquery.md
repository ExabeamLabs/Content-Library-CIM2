#### Parser Content
```Java
{
Name = "splunk-stream-json-dns-request-success-query"
ExtractionType = json
Vendor = "Splunk"
Product = "Splunk Stream"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Conditions = [
""""query":"""
""":dns""""
""""message_type""""
]
Fields = [
  """exa_json_path=$.timestamp,exa_field_name=time"""
  """exa_json_path=$.bytes,exa_field_name=bytes"""
  """exa_json_path=$.bytes_in,exa_field_name=bytes_in"""
  """exa_json_path=$.bytes_out,exa_field_name=bytes_out"""
  """exa_json_path=$.dest_ip,exa_field_name=dest_ip"""
  """exa_json_path=$.dest_mac,exa_field_name=dest_mac"""
  """exa_json_path=$.dest_port,exa_field_name=dest_port"""
  """exa_json_path=$.src_ip,exa_field_name=src_ip"""
  """exa_json_path=$.src_mac,exa_field_name=src_mac"""
  """exa_json_path=$.src_port,exa_field_name=src_port"""
  """exa_json_path=$.time_taken,exa_field_name=time_taken"""
  """exa_json_path=$.transport,exa_field_name=protocol"""
  """exa_json_path=$.ttl,exa_field_name=response_ttl"""
  """exa_json_path=$.query.[0],exa_field_name=dns_query"""
  """exa_json_path=$.query_type.[0],exa_field_name=dns_query_type"""
  """exa_json_path=$.host_addr,exa_field_name=host"""
  """exa_json_path=$.host_name,exa_field_name=host"""
]
ParserVersion = "v1.0.0"


}
```