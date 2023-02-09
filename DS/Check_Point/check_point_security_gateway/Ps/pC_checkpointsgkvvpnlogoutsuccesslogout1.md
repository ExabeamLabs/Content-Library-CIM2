#### Parser Content
```Java
{
Name = checkpoint-sg-kv-vpn-logout-success-logout-1
  Vendor = Check Point 
  Product = Check Point Security Gateway
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """|product=Connectra|""", """|event_type=Logout|""" ]
  Fields = [
    """\|(U|u)ser=({first_name}[^,@\|]+),\s*({last_name}[^@\|]+)@({domain}[^\s\|]+)\s*\(({user}[^\)\|]+)\)""",
    """\|user_dn=({user_ou}[^\|]+)\|""",
    """\|time=({time}\d+\w+\d\d\d\d \d+:\d+:\d+)""",
    """\|src=(?:({src_ip}[a-fA-F\d.:]+)|({src_host}[\w.\-]+))\|""",
    """\|reason=({failure_reason}[^\|]+)\|"""
  ]
  ParserVersion = "v1.0.0"


}
```