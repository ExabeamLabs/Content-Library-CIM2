#### Parser Content
```Java
{
Name = darktrace-darktrace-json-app-login-fail-failedlogin
 ParserVersion = v1.0.0
 Product = Darktrace
 Vendor = Darktrace
 TimeFormat ="yyyy-MM-dd HH:mm:ss"
 ExtractionType = json
 Conditions =[ """endpoint":"/login""", """description":"""", """Failed login""", """method":"POST""" ]
 Fields = [
  """exa_json_path=$.username,exa_field_name=user"""
  """exa_regex="+endpoint"+:\s*"+\/*({operation}[^"]+)"""
  """exa_json_path=$.method,exa_field_name=method"""
  """exa_json_path=$.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.status,exa_field_name=result_code"""
  """exa_json_path=$.description,exa_field_name=additional_info"""
 ]


}
```