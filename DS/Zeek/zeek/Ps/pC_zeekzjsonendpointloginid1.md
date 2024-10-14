#### Parser Content
```Java
{
Name = "zeek-z-json-endpoint-login-id-1"
Vendor = "Zeek"
Product = "Zeek"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """"ntlm","""
  """"id.orig_h":"""
  """"id.resp_h":"""
]
Fields = [
  """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}Z)"""
  """"uid":"({connection_id}[^"]+)"""
  """"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"id\.orig_p":({src_port}\d+)"""
  """"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"id\.resp_p":({dest_port}\d+)"""
  """"hostname":"?({src_host}[^,"]+)"""
  """"username":"?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"username":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+)?)))""""
  """"success":({result}[^,]+)""",
  """exa_json_path=$.ts,exa_field_name=time""",
  """exa_json_path=$._system_name,exa_field_name=host""",
  """exa_json_path=$.uid,exa_field_name=connection_id""",
  """exa_regex="id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_regex="id\.orig_p\\?"+:({src_port}\d+)""",
  """exa_regex="id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """exa_regex="id\.resp_p\\?"+:({dest_port}\d+)""",
  """exa_json_path=$.hostname,exa_field_name=src_host""",
  """exa_json_path=$.username,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """exa_regex="username":"?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """exa_json_path=$.username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+)?)))""",
  """exa_regex="username":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+)?)))""""
  """exa_json_path=$.success,exa_field_name=result"""
]
ParserVersion = "v1.0.0"


}
```