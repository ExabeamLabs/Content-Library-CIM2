#### Parser Content
```Java
{
Name = citrix-netscalar-str-vpn-login-fail-loginfailed
  ParserVersion = v1.0.0
  Vendor = citrix
  Product = citrix netscaler
  TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
  Conditions = [ """LOGIN_FAILED""", """ Client_ip """ ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)""",
    """({time}\d\d/\d\d/\d\d\d\d:\d\d:\d\d:\d\d \w+)""",
    """User ({email_address}[^@\s]+@[^@\s]+) - Client_ip ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """User (({domain}[^\s\\]+)\\+)?({user}[^@\s\\]+) - Client_ip ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """ Failure_reason "({failure_reason}[^"]+)""",
    """Browser .*?({user_agent}[^"]+)"""
  ]


}
```