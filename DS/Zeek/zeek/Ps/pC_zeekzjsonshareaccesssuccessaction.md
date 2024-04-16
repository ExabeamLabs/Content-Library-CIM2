#### Parser Content
```Java
{
Name = "zeek-z-json-share-access-success-action"
Vendor = "Zeek"
Product = "Zeek"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """"id.orig_h"""
  """"id.resp_h"""
  """"action"""
  """"SMB::FILE_OPEN"""
]
Fields = [
  """exa_regex="HOST\"+:\s*\"+({host}[^\"]+)\""""
  """exa_regex="TAGS\"+:\s*\"+({event_code}[^\"]+)\""""
  """exa_json_path=$.ts,exa_field_name=time""",
  """exa_regex=SMB::({access}FILE_OPEN)"""
  """exa_regex="id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_regex="id\.orig_p\\?"+:({src_port}\d+)""",
  """exa_regex="id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """exa_regex="id\.resp_p\\?"+:({dest_port}\d+)""",
  """exa_json_path=$.path,exa_field_name=share_path""",
  """exa_json_path=$.name,exa_regex=({file_path}({file_dir}[^\"]*?(\\u005c|[\\\/])*)({file_name}[^\"\\\/]+?(\.({file_ext}[^\"\\\/\.]+))?))\s*"""",
  """exa_regex="name\\?\"+:\\?\"+({file_path}({file_dir}[^\"]*?(\\u005c|[\\\/])*)({file_name}[^\"\\\/]+?(\.({file_ext}[^\"\\\/\.]+))?))\s*"""",
  """exa_json_path=$.size,exa_field_name=bytes"""
]
ParserVersion = "v1.0.0"


}
```