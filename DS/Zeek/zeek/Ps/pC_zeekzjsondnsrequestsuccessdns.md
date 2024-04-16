#### Parser Content
```Java
{
Name = "zeek-z-json-dns-request-success-dns"
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
ExtractionType = json
Conditions = [
""""id.orig_h":"""
""""id.resp_h":"""
""""dns","""
""""qtype_name":"""
]
Fields = [
  """"_system_name":"({host}[\w\-.]+)""",
  """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
  """"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"id\.orig_p":({src_port}\d+)""",
  """"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"id\.resp_p":({dest_port}\d+)""",
  """"proto":"({protocol}[^"]+)""",
  """"query":"({query}[^"]+)"""",
  """"qtype_name":"({dns_query_type}[^"]+)""",

  """exa_json_path=$._system_name,exa_regex=^({host}[\w\-.]+)$""",
  """exa_json_path=$.ts,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
  """exa_json_path=$.['id.orig_h'],exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
  """exa_json_path=$.['id.orig_p'],exa_field_name=src_port""",
  """exa_json_path=$.['id.resp_h'],exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
  """exa_json_path=$.['id.resp_p'],exa_field_name=dest_port""",
  """exa_json_path=$.proto,exa_field_name=protocol""",
  """exa_json_path=$.query,exa_field_name=query""",
  """exa_json_path=$.qtype_name,exa_field_name=dns_query_type"""
]
ParserVersion = "v1.0.0"


}
```