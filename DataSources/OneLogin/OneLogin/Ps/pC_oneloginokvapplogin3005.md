#### Parser Content
```Java
{
Name = onelogin-o-kv-app-login-3005
Vendor = "OneLogin"
Product = "OneLogin"
TimeFormat = "yyyy-MM-dd HH:mm:ss z"
Conditions = [
  """"actor_user_name":""""
  """"ipaddr":""""
  """"event_type_id":"""
]
Fields = [
  """"event_timestamp":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\s\w{1,3})""""
  """"actor_user_name":"({full_name}[^"]+)""""
  """"event_type_id":({activity_code}\d+)"""
  """"ipaddr":"({src_ip}[a-fA-F\d:.]+)""""
  """"app_name":"({app}[^"]+)""""
  """"notes":"({additional_info}[^"]+)""""
  """"user_agent":"({user_agent}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```