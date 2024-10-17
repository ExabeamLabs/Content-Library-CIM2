#### Parser Content
```Java
{
Name = "cisco-duo-sk4-vpn-login-success-newenrollment"
Product = "Duo Access"
Conditions = [
""" destinationServiceName =DUO """
"""VPN"""
""""new_enrollment""""
]
ParserVersion = "v1.0.0"

SSSSSSZ"]
  Fields = [
    """"ts"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)""",
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\|({operation}[^\|]+)\|\{""",
    """\|({full_name}({first_name}[^\s"\|]+)\s({last_name}[^"\|]+))\|[^\|]*\|\{""",
    """"name":\s*"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"email":\s*"({email_address}[^@"]+@({email_domain}[^"\s]+))"""",
    """"(phone|number)":\s*"({object}[^"]+)"""",
    """"role":\s*"({role}[^"]+)"""",
    """"status":\s*"({status_msg}[^"]+)"""",
    """({app}duo)""",
  
}
```