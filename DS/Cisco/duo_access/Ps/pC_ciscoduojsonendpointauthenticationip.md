#### Parser Content
```Java
{
Name = cisco-duo-json-endpoint-authentication-ip
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "epoch_sec"
  Conditions = [ """"new_enrollment"""",""""ip"""",""""result""""]
  Fields = [
    """"host":\s*"({host}[^"]+)""""
    """"timestamp":\s*({time}\d{10})""",
    """"device":\s*"*(null\}?|({device_name}[^",]+))"""",
    """"+ip"+:\s"+(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
    """"username"\s*:\s*"(?:({domain}[^\\"]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""",
    """"factor"\s*:\s*"(?:n\/a|({auth_method}[^"]+))"""",
    """"os"\s*:\s*"({os}[^"]+)"""",
    """"os_version"\s*:\s*"({os_version}[^"]+)"""",
    """"browser"\s*:\s*"({browser}[^"]+)"""",
    """"browser_version"\s*:\s*"({browser_version}[^"]+)"""",
    """"result"\s*:\s*"({action}[^"]+)"""",
    """"reason"\s*:\s*"({failure_reason}[^"]+)"""",
    """"new_enrollment"\s*:\s*({new_enrollment}true|false)""",
    """"*integration"*:\s*"*({service_name}[^"]+)""",
    """"email":\s*"({email_address}[^@"]+@[^"]+)"""",
    """"location":.+?"country": "({mfa_country}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```