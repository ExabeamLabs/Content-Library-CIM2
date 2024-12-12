#### Parser Content
```Java
{
Name = cisco-duo-str-endpoint-authentication-bypassedduo2fa
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = [ "MMM  d HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [""" login_duo: """, """ User """, """ bypassed Duo 2FA due to """]
  Fields = [
    """({time}\w{3}\s+\d\d?\s\d\d:\d\d:\d\d)"""
    """\s\d\d:\d\d:\d\d\s+({host}[\w.-]+)""",
    """({operation_type}login_duo)"""
    """({event_name}User.+?group)"""
    """User ({user}[^\s]+)"""
    """({operation}bypassed Duo 2FA)"""
    """user's ({group_name}.+?)\sgroup"""
  ]
  ParserVersion = "v1.0.0"


}
```