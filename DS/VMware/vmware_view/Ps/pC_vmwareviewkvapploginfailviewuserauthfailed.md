#### Parser Content
```Java
{
Name = "vmware-view-kv-app-login-fail-viewuserauthfailed"
  ParserVersion = "v1.0.0"
  Vendor = "VMware"
  Product = "VMware View"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """ View - """, """_USER_AUTHFAILED""", """Severity="AUDIT_FAIL"""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+\d+\s+""",
    """\s+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """({app}View)""",
    """\s+({dest_host}[^\s]+)\s+View - """,
    """\s+ClientIpAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """UserDisplayName ="(({domain}[^"\\]+)\\)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """USER_AUTHFAILED_({failure_reason}[^"]+)""""
   ]


}
```