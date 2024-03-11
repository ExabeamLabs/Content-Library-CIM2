#### Parser Content
```Java
{
Name = checkpoint-sg-kv-vpn-login-fail-loginfailure
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point Security Gateway
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """,cvpn_category=Session,""", """,product=Connectra,""", """,status=Failure,""", """,event_type=Login,""" ]
  Fields = [
    """\,(U|u)ser=({user}[^\,]+)""",
    """\,user_dn=({user_ou}[^\,]+)""",
    """\s+time=({time}\d+\w+\s+\d+:\d+:\d+)""",
    """\,reason=({failure_reason}[^\,]+\S)\s*\,""",
    """\,src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\,user_group=({realm}[^\,]+)""",
    """\,Hostname=({host}[^\,]+)""",
  ]


}
```