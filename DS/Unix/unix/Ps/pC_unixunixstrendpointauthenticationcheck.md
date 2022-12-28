#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-authentication-check
  ParserVersion = "v1.0.0"
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """pam_unix(sshd:auth): check pass;""" ]
  Fields = [
    """({host}[\w.\-]+)\s+sshd\[""",
    """check pass; user (unknown|({user}\S+))""",
  ]


}
```