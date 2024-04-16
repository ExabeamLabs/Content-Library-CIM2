#### Parser Content
```Java
{
Name = zeek-z-json-dns-response-success-rcode
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ 
""""id.orig_h"""
""""id.resp_h"""
""""rcode"""
""""rcode_name"""
]
  Fields = [
    """exa_json_path=$._system_name,exa_field_name=host""",
    """exa_json_path=$.ts,exa_field_name=time""",
    """exa_json_path=$.uid,exa_field_name=connection_id""",
    """exa_regex="id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex="id\.orig_p\\?"+:({src_port}\d+)""",
    """exa_regex="id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_regex="id\.resp_p\\?"+:({dest_port}\d+)""",
    """exa_json_path=$.proto,exa_field_name=protocol""",
    """exa_json_path=$.query,exa_field_name=dns_query""",
    """exa_json_path=$.qtype_name,exa_field_name=dns_query_type""",
    """exa_json_path=$.rcode_name,exa_field_name=dns_response_code""",
    """exa_json_path=$.answers,exa_regex=\[({dns_response}.+?)\]""",
    """exa_json_path=$.rejected,exa_field_name=result"""
  ]


}
```