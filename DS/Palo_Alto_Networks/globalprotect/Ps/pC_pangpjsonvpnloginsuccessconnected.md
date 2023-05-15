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
  """"PrivateIPv(4|6)":"({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """"PublicIPv(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """"LogType":"({app}[^"]+)""""
  """"EventStatus":"({result}[^"]+)""""
  """"EndpointDeviceName":"({src_host}[\w\-\.]+)""""
  """"SourceRegion":"({src_country}[^"]+)""""
  """"(Source)?User(Name)?":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+))""""
  """"EndpointOSType":"({os}[^"]+)""""
  """"EventIDValue":"({event_name}[^"]+)""""
  """"AuthMethod":"?((?i)null|({auth_method}[^,"]+))"""
  """"Description":"({additional_info}[^"]+:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))""""
  ]
  ParserVersion = "v1.0.0"


}
```