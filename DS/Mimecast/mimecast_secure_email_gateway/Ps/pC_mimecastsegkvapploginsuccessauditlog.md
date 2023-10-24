#### Parser Content
```Java
{
Name = mimecast-seg-kv-app-login-success-auditlog
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ Application:""", """|action=""", """|auditType=""", """|mcType=auditLog|""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-].+?)\|""",
    """\|user=(|({email_address}[^@\|]+@({email_domain}[^@\|]+\.[^\|]+))|({user}[\w\.\-]{1,40}\$?))\|""",
    """\sApplication:\s*({app}[^,]*)(,|\s*$)""",
    """\|app=(|({app}.+?))\|""",
    """\sIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(,|\s*$)""",
    """\|src=(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\|""",
    """\|action=(|({action}.+?))\|"""
  ]


}
```