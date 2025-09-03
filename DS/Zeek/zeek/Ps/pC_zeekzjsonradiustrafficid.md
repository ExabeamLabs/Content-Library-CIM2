#### Parser Content
```Java
{
Name = "zeek-z-json-radius-traffic-id"
Vendor = "Zeek"
Product = "Zeek"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """"id.orig_h":"""
  """"id.resp_h":"""
  """"radius","""
]
Fields = [
  """exa_json_path=$.ts,exa_field_name=time""",
  """exa_json_path=$.uid,exa_field_name=connection_id""",
  """exa_regex="id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_regex="id\.orig_p\\?"+:({src_port}\d+)""",
  """exa_regex="id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """exa_regex="id\.resp_p\\?"+:({dest_port}\d+)""",
  """exa_json_path=$.result,exa_field_name=result"""
]
ParserVersion = "v1.0.0"


}
```