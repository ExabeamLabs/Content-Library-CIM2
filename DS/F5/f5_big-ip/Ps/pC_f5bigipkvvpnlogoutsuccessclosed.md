#### Parser Content
```Java
{
Name = f5-bigip-kv-vpn-logout-success-closed
  Vendor = F5
  Product = F5 BIG-IP
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """ PPP tunnel """, """ closed.""", """Session_ID="""" ]
  Fields = [
  """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}(\+|-)\d{2}:\d{2})\s({host}[\w.-]+)""",
    """session_id="({session_id}[^\s="]+)"""",
    """\sAccess_Profile="({access_group}[^"]+)""""
  ]


}
```