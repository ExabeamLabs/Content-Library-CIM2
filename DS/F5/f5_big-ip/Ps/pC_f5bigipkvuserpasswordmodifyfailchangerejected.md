#### Parser Content
```Java
{
Name = f5-bigip-kv-user-password-modify-fail-changerejected
  Vendor = F5
  Product = F5 BIG-IP
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"VPN"""", """Password change rejected""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}(\+|-)\d{2}:\d{2})\s({host}[\w.-]+)""",
    """change password for '({dest_user}[^']+)' failed""",
    """({event_name}Password change rejected)"""
    """\sAccess_Profile="({access_group}[^"]+)""""
  ]


}
```