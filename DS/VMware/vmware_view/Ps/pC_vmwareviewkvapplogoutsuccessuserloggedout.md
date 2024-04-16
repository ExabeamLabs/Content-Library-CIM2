#### Parser Content
```Java
{
Name = vmware-view-kv-app-logout-success-userloggedout
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = VMware View
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """ View - """, """_USERLOGGEDOUT""", """Severity="AUDIT_SUCCESS"""" ]
  Fields = [
    """\s+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """\s+({dest_host}[^\s]+)\s+View - """,
    """UserDisplayName ="(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""",
    """EventType="({event_category}[^"]+)""",
    """Severity="({result}[^"]+)""",
  ]


}
```