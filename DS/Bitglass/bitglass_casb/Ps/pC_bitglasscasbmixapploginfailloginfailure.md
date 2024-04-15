#### Parser Content
```Java
{
Name = "bitglass-casb-mix-app-login-fail-loginfailure"
Vendor = "Bitglass"
Product = "Bitglass CASB"
TimeFormat = "dd MMM yyyy HH:mm:ss"
Conditions = [
  """"activity":"""
  """"Failure, Login""""
  """api.bitglass.com"""
]
Fields = [
  """"time":\s*"({time}\d+ \w+ \d\d\d\d \d\d:\d\d:\d\d)"""
  """"instancename":\s*"({host}[^"]+)""""
  """"user":\s*"({user}[^"\s@]+)""""
  """"user":\s*"({full_name}[^"\s@]+\s+[^"\s@]+)""""
  """"email":\s*"({email_address}[^"]+)""""
  """"application":\s*"({app}[^"]+)""""
  """"ipaddress":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"useragent":\s*"({user_agent}.+?)","""
  """"details":\s*"({failure_reason}.+?)","""
]
ParserVersion = "v1.0.0"


}
```