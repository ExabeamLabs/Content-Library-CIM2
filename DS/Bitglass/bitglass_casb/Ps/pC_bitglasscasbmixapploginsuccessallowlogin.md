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
Fields = [
  """"time":\s*"({time}\d+ \w+ \d\d\d\d \d\d:\d\d:\d\d)"""
  """"instancename":\s*"({host}[^"]+)""""
  """"user":\s*"({user}[\w\.\-]{1,40}\$?)""""
  """"user":\s*"({full_name}[^"\s@]+\s+[^"\s@]+)""""
  """"email":\s*"({email_address}[^@]+@({email_domain}[^"]+))""""
  """"application":\s*"({app}[^"]+)""""
  """"ipaddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"useragent":\s*"({user_agent}.+?)","""
]
ParserVersion = "v1.0.0"


}
```