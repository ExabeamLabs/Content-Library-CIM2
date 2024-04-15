#### Parser Content
```Java
{
Name = "mimecast-seg-cef-app-login-fail-logonauthfailed"
  ParserVersion = "v1.0.0"
  Vendor = "Mimecast"
  Product = "Mimecast Secure Email Gateway"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =Mimecast Email Security""", """Logon Authentication Failed""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w.\-]+ """,
    """IP:\s({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}),""",
    """"user":"(|({email_address}[^@]+@[^"]+?))"""",
    """\sReason:\s(|({failure_reason}[^=]+?))(\s+\w+=|\s*$)""",
    """\sApplication:\s*({app}[^,]+?),""",
    """"user":"({email_address}[^"]+)"""
  ]


}
```