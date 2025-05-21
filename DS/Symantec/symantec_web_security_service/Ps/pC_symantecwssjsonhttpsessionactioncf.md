#### Parser Content
```Java
{
Name = "symantec-wss-json-http-session-actioncf"
ExtractionType = json
Vendor = "Symantec"
Product = "Symantec Web Security Service"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""filter_result_CF"""
"""action_CF"""
"""BlueCoat_CL"""
]
Fields = [
  """exa_json_path=$.TimeGenerated,exa_field_name=time"""
  """exa_json_path=$.Computer,exa_field_name=host"""
  """exa_json_path=$.user_CF,exa_field_name=user"""
  """exa_json_path=$.user_agent_CF,exa_regex=(-|({user_agent}[^"]+))"""
  """exa_json_path=$.country_CF,exa_field_name=country"""
  """exa_json_path=$.app_CF,exa_regex=(none|({app}[^"]+))"""
  """exa_json_path=$.src_CF,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.action_CF,exa_regex=(-|({proxy_action}[^"]+))"""
  """exa_json_path=$.method_CF,exa_field_name=method"""
  """exa_json_path=$.status_CF,exa_field_name=http_response_code"""
  """exa_json_path=$.uri_query_CF,exa_regex=(-|({uri_query}[^"]+))"""
  """exa_json_path=$.url_CF,exa_regex=(-|({url}[^"]+))"""
  """exa_json_path=$.filter_result_CF,exa_regex=(-|({action}[^"]+))"""
  """exa_json_path=$.protocol_CF,exa_regex=(-|({protocol}[^"]+))"""
  """exa_json_path=$.bytes_sent_CF,exa_regex=(-|({bytes_out}\d+))"""
  """exa_json_path=$.bytes_recieved_CF,exa_regex=(-|({bytes_in}\d+))"""
  """exa_json_path=$.dport_CF,exa_regex=(-|({dest_port}\d+))"""
  """exa_json_path=$.proxy_ip_CF,exa_regex=(-|({proxy_ip_CF}[^"]+))"""
  """exa_json_path=$.['_ResourceId'],exa_regex=(-|({resource_id}[^"]+))"""
  """exa_json_path=$.Type,exa_regex=(-|({category}[^"]+))"""
  """exa_json_path=$.categories_CF,exa_regex=(-|({category}[^"]+))"""
  """exa_json_path=$.content_type_CF,exa_regex=(-|({mime}[^"]+))"""
]
ParserVersion = "v1.0.0"


}
```