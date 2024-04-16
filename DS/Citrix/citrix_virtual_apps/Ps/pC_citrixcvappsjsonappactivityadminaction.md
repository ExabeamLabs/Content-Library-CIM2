#### Parser Content
```Java
{
Name = citrix-cvapps-json-app-activity-adminaction
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Virtual Apps
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"event":"admin-action"""", """"system":"Citrix-XenApp"""", """"adminmachineip":"""", """"adminaccountname":"""" ]
  Fields = [
    """exa_json_path=$.starttime,exa_field_name=time""",
    """exa_json_path=$.username,exa_regex=(({email_address}[^@"]+@[^\."]+\.[^"]+)|(({domain}[^\\"]+)\\+)?({user}[\w\.\-]{1,40}\$?))""",
    """exa_json_path=$.text,exa_field_name=additional_info""",
    """exa_regex="adminaccountname":"(({account_domain}[^\\"]+)\\+)?({account_name}[^"]+)",""",
    """exa_regex=({event_name}admin-action)"""
  ]


}
```