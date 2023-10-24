#### Parser Content
```Java
{
Name = cisco-duo-json-endpoint-authentication-result-1
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "epoch_sec"
  ParserVersion = "v1.0.0"
  Conditions = [ """"eventtype":"authentication"""",""""result"""" ]
  Fields = [
    """"timestamp":({time}\d{10})""",
    """"host":"+({host}[\w\-\.]+)"""",
    """"ip":"+(0.0.0.0|null|({src_ip}[a-fA-F:\.\d]+))"""",
    """"result":"({action}[^"]+)"""",
    """"reason":"({failure_reason}[^"]+)"[^=]+?"result":"(denied|fraud)"""",
    """"result":"(denied|fraud)"[^=]+?"reason":"({failure_reason}[^"]+)"""",
    """"os":"({os}[^"]+)"""",
    """"os_version":"({os_version}[^"]+)"""",
    """"browser":"(Unknown|({browser}[^"]+))"""",
    """"browser_version":"({browser_version}[^"]+)"""",
    """"email":"({email_address}[^@"]+@[^"]+)"""",
    """"factor":"(?:n\/a|({auth_method}[^"]+))"""",
    """"user":[^\}]+?"name":"({user}[\w\.\-]{1,40}\$?)""""
    """"new_enrollment"\s*:\s*({new_enrollment}true|false)""",
    """"application".+?"name":\s*"({service_name}[^"]+)"""
    """"location":.+?"country":\s*"({src_country}[^"]+)"""
  ]


}
```