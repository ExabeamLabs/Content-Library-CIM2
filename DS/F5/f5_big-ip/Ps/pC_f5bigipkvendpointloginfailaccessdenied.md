#### Parser Content
```Java
{
Name = f5-bigip-kv-endpoint-login-fail-accessdenied
  Vendor = F5
  Product = F5 BIG-IP
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"VPN"""", """SECURID_AUTH_STATE_ACCESS_DENIED""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}(\+|-)\d{2}:\d{2})\s({host}[\w.-]+)""",
    """authentication with '({user}[\w\.\-\!\#\^\~]{1,40}\$?)' failed""",
    """Error_Message="({event_name}[^\."]+)"""
    """\sAccess_Profile="({access_group}[^"]+)""""
  ]


}
```