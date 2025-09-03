#### Parser Content
```Java
{
Name = "vmware-view-kv-app-login-success-viewuserloggedin"
  ParserVersion = "v1.0.0"
  Vendor = "VMware"
  Product = "VMware View"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """ View - """, """_USERLOGGEDIN""", """Severity="AUDIT_SUCCESS"""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+\d+\s+""",
    """({app}View)""",
    """\s+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """\s+ForwardedClientIpAddress="[^"]*?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\s+({dest_host}[^\s]+)\s+View - """,
    """UserDisplayName ="(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
   ]


}
```