#### Parser Content
```Java
{
Name = cisco-duo-json-endpoint-authentication-result
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "epoch_sec"
  Conditions = [ """"eventtype": "authentication"""",""""result""""]
  Fields = [
    """"+timestamp"+:\s({time}\d{10})""",
    """"+host"+:\s"+({host}[\w\-\.]+)"""",
    """"+ip"+:\s"+(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
    """"+username"+:\s*"(?:({domain}[^\\]+))?({user}[\w\.\-]{1,40}\$?)"""",
    """"+integration"+:\s"+({auth_method}[^"]+)"""",
    """"+device"+:\s(null|"+({device_name}[^"]+))""",
    """"+result"+:\s"+({action}[^"]+)"""",
    """"+reason"+:\s"+({failure_reason}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```