#### Parser Content
```Java
{
Name = bitglass-casb-cef-app-logout-activity
  ParserVersion = v1.0.0
  Vendor = Bitglass
  Product = Bitglass CASB
  TimeFormat = "dd MMM yyyy HH:mm:ss"
  Conditions = [ """"activity":""", """"Logout"""", """api.bitglass.com""" ]
  Fields = [
    """"instancename":\s*"({host}[^"]+)"""",
    """"time":\s*"({time}\d+ \w+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """"user":\s*"({user}[^"\s@]+)"""",
    """"user":\s*"({full_name}[^"\s@]+\s+[^"\s@]+)"""",
    """"email":\s*"({email_address}[^"]+)"""",
    """"device":\s*"({os}[^"]+)"""",
    """"application":\s*"({app}[^"]+)"""",
    """"ipaddress":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"useragent":\s*"({user_agent}.+?)",""",
    """"useragent":\s*".+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident)""""
  ]


}
```