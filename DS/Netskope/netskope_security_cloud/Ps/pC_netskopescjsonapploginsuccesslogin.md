#### Parser Content
```Java
{
Name = "netskope-sc-json-app-login-success-login"
Vendor = "Netskope"
Product = "Netskope Security Cloud"
TimeFormat = "epoch_sec"
ExtractionType = json
Conditions = [
"""session_begin"""
"""activity": "Login Successful"""
]
Fields = [
  """exa_json_path=$.timestamp,exa_field_name=time"""
  """exa_json_path=$.dstip,exa_field_name=host"""
  """exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_json_path=$.app,exa_field_name=app"""
  """exa_json_path=$.dstip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """exa_json_path=$.srcip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.browser,exa_field_name=browser,exa_match_expr=!InList(toLower($.browser),"unknown")"""
  """exa_json_path=$.os,exa_field_name=os,exa_match_expr=!InList(toLower($.os),"unknown")"""
  """exa_json_path=$.access_method,exa_field_name=auth_method"""
  """exa_json_path=$.object,exa_field_name=object"""
]
ParserVersion = "v1.0.0"


}
```