#### Parser Content
```Java
{
Name = sybase-s-json-database-logout-logout
  Vendor = Sybase
  Product = Sybase
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """object_name""", """"event_desc"""", """"logout"""", """"database_name"""", """"extra_info"""" ]
  Fields = [
     """"extra_info"+:"+\s*({additional_info}[^"]+?)\s*"""",
     """"database_name"+:"+({db_name}[^"]+?)"""",
     """"object_name"+:"+({db_object}[^"]+?)"""",
     """"event_desc"+:"+({event_name}[^"]+?)"""",
     """"object_owner"+:"+({db_user}[^"]+?)"""",
     """"facets_environment"+:"+({host}[^"]+?)"""",
     """"event_time"+:"+({time}[^"]+?)"""",
     """"user_name"+:"+({user}[^"]+?)""""
  ]
  ParserVersion = "v1.0.0"


}
```