#### Parser Content
```Java
{
Name = pan-gp-json-endpoint-notification-success-hostinfo
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"EventStatus":"success"""", """"AuthMethod":""", """Stage":"host-info"""", """GLOBALPROTECT""", """"EventIDValue":"""" ]
  Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)"""
  """"DeviceName":"({host}[\w\-\.]+)"""
  """"PrivateIPv(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"PublicIPv(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"LogType":"({app}[^"]+)""""
  """"EventStatus":"({result}[^"]+)""""
  """"EndpointDeviceName":"?(null|({src_host}[\w\-\.]+))""""
  """"SourceRegion":"({src_country}[^"]+)""""
  """"(Source)?User(Name)?":"?((?i)null|pre-logon|(({email_address}[^\@,"]+@[^\.,"]+\.[^,"]+)|({user}[\w\.\-]{1,40}\$?)))""""
  """"EndpointOSType":"({os}[^"]+)""""
  """"EventIDValue":"({event_name}[^"]+)""""
  """"AuthMethod":"?((?i)null|({auth_method}[^,"]+))"""
  """"Description":"({additional_info}[^"]+)""""  
  ]
  ParserVersion = v1.0.0


}
```