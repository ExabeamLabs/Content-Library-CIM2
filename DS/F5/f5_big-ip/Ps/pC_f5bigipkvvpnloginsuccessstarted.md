#### Parser Content
```Java
{
Name = f5-bigip-kv-vpn-login-success-started
  Vendor = F5
  Product = F5 BIG-IP
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """ PPP tunnel """, """ started.""", """Session_ID="""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}(\+|-)\d{2}:\d{2})\s({host}[\w.-]+)""",
    """session_id="({session_id}[^\s="]+)""""
  ]


}
```