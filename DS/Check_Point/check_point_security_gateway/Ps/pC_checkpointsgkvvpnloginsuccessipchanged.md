#### Parser Content
```Java
{
Name = checkpoint-sg-kv-vpn-login-success-ipchanged
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point Security Gateway
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """,cvpn_category=Session,""", """,product=Connectra,""", """,action=ip changed,""" ]
  Fields = [
    """\,(U|u)ser=({user}[^\,]+)""",
    """\s+time=({time}\d+\w+\s+\d+:\d+:\d+)""",
    """\,src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """\,assigned_IP:=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\,orig=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  ]


}
```