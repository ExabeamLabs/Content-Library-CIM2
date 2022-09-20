#### Parser Content
```Java
{
Name = checkpoint-ia-kv-vpn-login-success-login
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Identity Awareness
  TimeFormat = "dMMMyyyy H:mm:ss"
  Conditions = [ """Product=Identity Awareness""" , """Login""", """Source=""", """User="""]
  Fields = [
    """src_user_group=(-|({user_group_name}[^\|]+))\|""",
    """auth_method=(-|({auth_method}[^\|]+))\|""",
    """auth_status=(-|({action}Successful|Failed))""",
    """\s+({time}\d{1,2}\w+\d\d\d\s\d{1,2}:\d{1,2}:\d{1,2})\|""",
    """Originip=({host}[^\|]+)\|""",
    """Origin=({host}[^\|]+)\|""",
    """Action=(-|({operation}[^\|]+))\|""",
    """SIP=({src_ip}[^\|]+)\|""",
    """SPort=({src_port}\d+)""",
    """DPort=({dest_port}\d+)""",
    """Destination=(-|({dest_host}[^\|]+))\|""",
    """DIP=(-|({dest_ip}[^\|]+))\|""",
    """Protocol=(-|({protocol}[^\|]+))\|""",
    """IFDirection=(-|({direction}[^\|]+))\|""",
    """Reason=(-|({reason}[^\|]+))\|""",
    """(U|u)ser=(-|({full_name}[^\(]+)\s+\(({user}[^\)]+))""",
    """domain_name=(-|({domain}[^\|]+))\|""",
    """termination_reason=(-|({failure_reason}[^\|]+))\|""",
    """duration=(-|({session_duration}[^\|]+))\|""",
    """description=(-|({additional_info}[^\|]+))\|""",
  ]


}
```