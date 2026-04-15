#### Parser Content
```Java
{
Name = github-g-json-user-invite-success-invitemember
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "epoch"
  ExtractionType = json
  Conditions = [ """"action":"org.invite_member"""", """"org":"""" ]
  Fields = [
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.action,exa_field_name=operation""",
    """exa_json_path=$.actor,exa_field_name=user""",
    """exa_json_path=$..external_identity_username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$..external_identity_nameid,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.email,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.invitee_email,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.user_agent,exa_field_name=user_agent""",
    """exa_json_path=$.org,exa_field_name=company""",
    """exa_json_path=$.actor_ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$.actor_location.country_code,exa_field_name=country_code"""
  ]


}
```