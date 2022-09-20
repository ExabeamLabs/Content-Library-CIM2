#### Parser Content
```Java
{
Name = checkpoint-sg-kv-vpn-login-fail-loginfailure
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Security Gateway
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """,cvpn_category=Session,""", """,product=Connectra,""", """,status=Failure,""", """,event_type=Login,""" ]
  Fields = [
    """\,(U|u)ser=({user}[^\,]+)""",
    """\,user_dn=({user_ou}[^\,]+)""",
    """\s+time=({time}\d+\w+\s+\d+:\d+:\d+)""",
    """\,reason=({failure_reason}[^\,]+\S)\s*\,""",
    """\,src=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\,user_group=({realm}[^\,]+)""",
    """\,Hostname=({host}[^\,]+)""",
  ]


}
```