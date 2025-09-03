#### Parser Content
```Java
{
Name = secomea-s-str-app-login-success-login
 ParserVersion = "v1.0.0"
 Vendor = Secomea
 Product = Secomea
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
 Conditions = [ """ AUDIT - - - """, """: Login """, """. From: """ ]
 Fields = [
  """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
  """\s({host}[^\s]+) AUDIT - - - (({domain}\S+)|[^\\]+)\\({user_id}[^\(]+)\s\(({full_name}[^\)]+)?\)\: ({action}Login)\s""",
  """\sFrom\:\s(({src_ip}[A-Fa-f\d.:]{1,2000})|({src_host}\S+))"""
    ]
  DupFields = [ "action->operation" ]


}
```