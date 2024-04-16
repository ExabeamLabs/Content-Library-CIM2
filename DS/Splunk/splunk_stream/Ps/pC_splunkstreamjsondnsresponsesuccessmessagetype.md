#### Parser Content
```Java
{
Name = "splunk-stream-json-dns-response-success-messagetype"
ExtractionType = json
Vendor = "Splunk"
Product = "Splunk Stream"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Conditions = [
""""reply_code":"""
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
  """exa_json_path=$.ttl.[0],exa_field_name=response_ttl"""
  """exa_json_path=$.query,exa_field_name=dns_query"""
  """exa_json_path=$.query_type,exa_field_name=dns_query_type"""
  """exa_json_path=$.reply_code,exa_field_name=dns_response_code"""
  """exa_json_path=$.host_addr,exa_field_name=host"""
  """exa_json_path=$.hostname[0],exa_field_name=host"""
]
ParserVersion = "v1.0.0"


}
```