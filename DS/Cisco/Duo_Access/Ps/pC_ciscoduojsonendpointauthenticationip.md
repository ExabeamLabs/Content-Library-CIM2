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
    """"timestamp":\s*({time}\d+)""",
    """"device":\s*"*(null\}?|({device_name}[^",]+))"""",
    """"+ip"+:\s"+(0.0.0.0|({src_ip}[a-fA-F:\.\d]+))"""",
    """"username"\s*:\s*"(?:({domain}[^\"]+)\\)?({user}[^"]+)"""",
    """"factor"\s*:\s*"(?:n\/a|({auth_method}[^"]+))"""",
    """"os"\s*:\s*"({os}[^"]+)"""",
    """"os_version"\s*:\s*"({os_version}[^"]+)"""",
    """"browser"\s*:\s*"({browser}[^"]+)"""",
    """"browser_version"\s*:\s*"({browser_version}[^"]+)"""",
    """"result"\s*:\s*"({action}[^"]+)"""",
    """"reason"\s*:\s*"({failure_reason}[^"]+)"""",
    """"new_enrollment"\s*:\s*({new_enrollment}true|false)""",
    """"*integration"*:\s*"*({service_name}[^"]+)"""
    """"email":\s*"({email_address}[^@"]+@[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```