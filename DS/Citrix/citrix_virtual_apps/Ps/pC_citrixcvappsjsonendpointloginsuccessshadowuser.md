#### Parser Content
```Java
{
Name = citrix-cvapps-json-endpoint-login-success-shadowuser
  Vendor = Citrix
  Product = Citrix Virtual Apps
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"text":"Shadow user""", """"event":"admin-action"""", """"system":"Citrix-XenApp""""]
  Fields = [
    """exa_json_path=$.starttime,exa_field_name=time""",
    """exa_json_path=$.username,exa_regex=(({email_address}[^@"]+@[^\."]+\.[^"]+)|(({domain}[^\\"]+)\\+)?({user}[\w\.\-]{1,40}\$?))""",
    """exa_regex=({event_name}admin-action)""",
    """exa_json_path=$.text,exa_field_name=additional_info""",
    """exa_regex="adminaccountname":"(({account_domain}[^\\"]+)\\+)?({account_name}[^"]+)","""
  ]
  ParserVersion = "v1.0.0"


}
```