#### Parser Content
```Java
{
Name = imanage-i-json-app-activity-success-checkout
ExtractionType = json
Vendor = iManage
Product = iManage
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"docnum":"""
  """"activity":"""
  """"docname":"""
  """"docsize":"""
]
Fields = [
  """exa_json_path=$.activity_datetime,exa_field_name=time""",
  """exa_json_path=$.employee_cms_code,exa_field_name=user_id,exa_match_expr=!InList(toLower($.employee_cms_code),"unknown")""",
  """exa_json_path=$.location,exa_regex=(UNKNOWN|({src_ip}(\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]*:[A-Fa-f\d:]+)|({src_host}[^"]+))""",
  """exa_json_path=$.docnum,exa_field_name=resource,exa_match_expr=!InList(toLower($.docnum),"unknown")""",
  """exa_json_path=$.fullname,exa_field_name=full_name,exa_match_expr=!InList(toLower($.fullname),"unknown")""",
  """exa_json_path=$.activity,exa_field_name=operation,exa_match_expr=!InList(toLower($.activity),"unknown")""",
  """exa_json_path=$.database,exa_field_name=app,exa_match_expr=!InList(toLower($.database),"unknown")""",
  """exa_json_path=$.docname,exa_field_name=object,exa_match_expr=!InList(toLower($.docname),"unknown")""",
  """exa_json_path=$.client_code,exa_field_name=client_id,exa_match_expr=!InList(toLower($.client_code),"unknown")""",
  """exa_json_path=$.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
  """exa_json_path=$.docuser,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
  """exa_json_path=$.appname,exa_field_name=app""",
  """exa_json_path=$.docloc,exa_regex=({file_path}({file_dir}([^"]+)?[\/\\])?({file_name}[^\/\\"]+))""",
]
ParserVersion = "v1.0.0"
},	 

{
Vendor = Imprivata
Product = Imprivata
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """\d\d:\d\d:\d\d ({host}[\w\-.]+) ({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """ServerIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """User:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """Event:\s*({operation}.+?)\s+ServerIP:"""
  """({app}Imprivata)"""
]
Name = imprivata-i-kv-app-activity-success-agentshutdown
Conditions = [
  """Event: Agent Shutdown"""
]
ParserVersion = "v1.0.0"


}
```