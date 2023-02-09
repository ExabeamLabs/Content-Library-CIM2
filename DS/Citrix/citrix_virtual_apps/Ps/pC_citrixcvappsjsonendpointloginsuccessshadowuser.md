#### Parser Content
```Java
{
Name = citrix-cvapps-json-endpoint-login-success-shadowuser
  Vendor = Citrix
  Product = Citrix Virtual Apps
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"text":"Shadow user""", """"event":"admin-action"""", """"system":"Citrix-XenApp""""]
  Fields = [
    """"starttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"username":"(({email_address}[^@"]+@[^\."]+\.[^"]+)|(({domain}[^\\"]+)\\+)?({user}[^"]+))"""",
    """({event_name}admin-action)""",
    """"text":"({additional_info}[^"]+)",""",
    """"adminaccountname":"(({account_domain}[^\\"]+)\\+)?({account_name}[^"]+)","""
  ]
  ParserVersion = "v1.0.0"


}
```