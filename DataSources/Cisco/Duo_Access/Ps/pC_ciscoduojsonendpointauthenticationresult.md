#### Parser Content
```Java
{
Name = cisco-duo-json-endpoint-authentication-result
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "epoch_sec"
  Conditions = [ """"eventtype": "authentication"""",""""result""""]
  Fields = [
    """"+timestamp"+:\s({time}\d+)""",
    """"+host"+:\s"+({host}[\w\-\.]+)"""",
    """"+ip"+:\s"+(0.0.0.0|({src_ip}[a-fA-F:\.\d]+))"""",
    """"+username"+:\s"+(({domain}[^\\]+)\\+)?({user}[^"]+)"""",
    """"+integration"+:\s"+({auth_method}[^"]+)"""",
    """"+device"+:\s(null|"+({device_name}[^"]+))""",
    """"+result"+:\s"+({action}[^"]+)"""",
    """"+reason"+:\s"+({failure_reason}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```