#### Parser Content
```Java
{
Name = mimecast-es-kv-app-login-success-auditlog
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Email Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ Application:""", """|action=""", """|auditType=""", """|mcType=auditLog|""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-].+?)\|""",
    """\|user=(|({user}.+?))\|""",
    """\|user=(|({email_address}[^@\|]+@({email_domain}[^@\|]+)))\|""",
    """\sApplication:\s*({app}[^,]*)(,|\s*$)""",
    """\|app=(|({app}.+?))\|""",
    """\sIP:\s*({src_ip}[a-fA-F\d.:]+)(,|\s*$)""",
    """\|src=(|({src_ip}[a-fA-F\d.:]+))\|""",
    """\|action=(|({action}.+?))\|"""
  ]


}
```