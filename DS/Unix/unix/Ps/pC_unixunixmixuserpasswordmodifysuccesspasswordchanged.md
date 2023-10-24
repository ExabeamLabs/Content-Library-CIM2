#### Parser Content
```Java
{
Name = unix-unix-mix-user-password-modify-success-passwordchanged
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""pam_unix(passwd:chauthtok):""",
"""password changed for"""
  ]
  Fields = [
"""\"agent_hostname\":\"(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[^\"]+)))\"""",
"""\d\d:\d\d:\d\dZ? (::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+)))""",
"""({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2})(\S+|Z)? (\d+|({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+))))"""
"""password changed for ({dest_user}.+?)\s*(\"|$)""", 
  ]


}
```