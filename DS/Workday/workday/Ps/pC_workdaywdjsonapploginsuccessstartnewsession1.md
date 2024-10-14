#### Parser Content
```Java
{
Name = workday-wd-json-app-login-success-startnewsession-1
  Vendor = Workday
  Product = Workday
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """:"workday"""", """"wd_systemaccount":""", """"wd_ipaddress":""",""""wd_activitycategory":""", """Start New Session""", """"wd_task":"""]
  Fields = [
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.agent.hostname,exa_field_name=host""",
    """exa_json_path=$.fields.device_product,exa_field_name=app""",
    """exa_regex=wd_systemaccount":"({domain}[^\/]+?)\s\/\s(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^\s,]+([\s,]+\s*[^\s"]+)+?))"""",
    """exa_json_path=$.wd_task,exa_field_name=operation""",
    """exa_json_path=$.wd_target,exa_field_name=object""",
    """exa_json_path=$.wd_useragent,exa_field_name=user_agent""",
    """exa_json_path=$.wd_ipaddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
   ]
   ParserVersion = v1.0.0


}
```