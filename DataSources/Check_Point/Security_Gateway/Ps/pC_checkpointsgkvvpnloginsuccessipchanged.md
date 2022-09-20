#### Parser Content
```Java
{
Name = checkpoint-sg-kv-vpn-login-success-ipchanged
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Security Gateway
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """,cvpn_category=Session,""", """,product=Connectra,""", """,action=ip changed,""" ]
  Fields = [
    """\,(U|u)ser=({user}[^\,]+)""",
    """\s+time=({time}\d+\w+\s+\d+:\d+:\d+)""",
    """\,assigned_IP:=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\,orig=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  ]


}
```