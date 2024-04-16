#### Parser Content
```Java
{
Name = sybase-s-json-database-login-success-login
Vendor = "Sybase"
Product = "Sybase"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """object_name"""
  """"event_desc""""
  """"login""""
  """"database_name""""
  """"extra_info""""
]
Fields = [
  """"database_name"+:"+({db_name}[^"]+?)""""
  """"object_name"+:"+({db_object}[^"]+?)""""
  """"event_desc"+:"+({event_name}[^"]+?)""""
  """"extra_info"+:"+\s*({additional_info}[^"]+?)\s*""""
  """"object_owner"+:"+({db_user}[^"]+?)""""
  """"facets_environment"+:"+({host}[^"]+?)""""
  """"event_time"+:"+({time}[^"]+?)""""
  """"user_name"+:"+({user}[\w\.\-]{1,40}\$?)""""
]
ParserVersion = "v1.0.0"


}
```