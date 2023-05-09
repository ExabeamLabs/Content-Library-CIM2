#### Parser Content
```Java
{
Name = pan-gp-json-vpn-login-success-connected
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"LogType":"GLOBALPROTECT"""", """"EventStatus":"success"""", """"AuthMethod":""", """"Stage":"connected"""" ]
  Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)"""
  """"DeviceName":"({host}[\w\-\.]+)"""
  """"PrivateIPv(4|6)":"({src_ip}[a-fA-F\d:.]+)""",
  """"PublicIPv(4|6)":"({dest_ip}[a-fA-F\d.:]+)"""
  """"LogType":"({app}[^"]+)""""
  """"EventStatus":"({result}[^"]+)""""
  """"EndpointDeviceName":"({src_host}[\w\-\.]+)""""
  """"SourceRegion":"({src_country}[^"]+)""""
  """"(Source)?User(Name)?":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+))""""
  """"EndpointOSType":"({os}[^"]+)""""
  """"EventIDValue":"({event_name}[^"]+)""""
  """"AuthMethod":"?((?i)null|({auth_method}[^,"]+))"""
  """"Description":"({additional_info}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```