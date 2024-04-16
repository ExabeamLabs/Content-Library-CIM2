#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-authentication-check
  ParserVersion = "v1.0.0"
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """pam_unix(sshd:auth): check pass;""" ]
  Fields = [
    """({time}\w+\s\d+\s\d\d:\d\d:\d\d)?\s*(::ffff:)?({host}\S+)? sshd\["""
    """>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """\d\d\s({host}[\w\-\.]+)(\s\w+)?\s*sshd\[""",
    """check pass; user (unknown|({user}[\w\.\-]{1,40}\$?))""",
  ]


}
```