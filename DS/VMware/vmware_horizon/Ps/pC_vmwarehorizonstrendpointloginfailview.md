#### Parser Content
```Java
{
Name = vmware-horizon-str-endpoint-login-fail-view
  Vendor = VMware
  Product = VMware Horizon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ View """, """failed to authenticate because of a bad username or password""" ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+View""",
    """User (?:({domain}[^\\\s]+)\\+)?({user}[^\\\s]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```