#### Parser Content
```Java
{
Name = pan-gp-json-app-activity-success-tunnel
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"EventStatus":"success"""", """"AuthMethod":""", """Stage":"tunnel"""", """LogType":"GLOBALPROTECT""", """"EventIDValue":"""" ]
  Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)"""
  """"DeviceName":"({host}[\w\-\.]+)"""
  """"PrivateIPv(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """"PublicIPv(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """"LogType":"({app}[^"]+)""""
  """"EventStatus":"({result}[^"]+)""""
  """"EndpointDeviceName":"?(null|({src_host}[\w\-\.]+))""""
  """"SourceRegion":"(\d\.\d\.\d\.\d|({src_country}[^"]+))""""
  """"(Source)?User(Name)?":"?((?i)null|pre-logon|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^,"]+)))""""
  """"EndpointOSType":"({os}[^"]+)""""
  """"EventIDValue":"({event_name}[^"]+)""""
  """"AuthMethod":"?((?i)null|({auth_method}[^,"]+))"""
  """"Description":"({additional_info}[^"]+)""""  
  ]
  DupFields = [ "event_name->operation" ]
  ParserVersion = "v1.0.0"


}
```