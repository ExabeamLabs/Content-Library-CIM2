#### Parser Content
```Java
{
Name = "bitglass-casb-mix-app-login-success-allowlogin"
Vendor = "Bitglass"
Product = "Bitglass CASB"
TimeFormat = "dd MMM yyyy HH:mm:ss"
Conditions = [
  """"activity":"""
  """"Login""""
  """api.bitglass.com"""
]
ExtractionType = json
Fields = [
  """"time":\s*"({time}\d+ \w+ \d\d\d\d \d\d:\d\d:\d\d)"""
  """"instancename":\s*"({host}[^"]+)""""
  """"user":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """"user":\s*"({full_name}[^"\s@]+\s+[^"\s@]+)""""
  """"email":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"application":\s*"({app}[^"]+)""""
  """"ipaddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"useragent":\s*"({user_agent}.+?)","""
  """exa_json_path=$.time,exa_field_name=time"""
  """exa_json_path=$.instancename,exa_field_name=host"""
  """exa_regex="user":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """exa_json_path=$.user,exa_field_name=full_name"""
  """exa_json_path=$.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.application,exa_field_name=app"""
  """exa_json_path=$.ipaddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.useragent,exa_field_name=user_agent"""
]
ParserVersion = "v1.0.0"


}
```