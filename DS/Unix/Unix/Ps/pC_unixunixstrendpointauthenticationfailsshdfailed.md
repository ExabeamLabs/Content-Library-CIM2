#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-authentication-fail-sshdfailed
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """sshd[""", """]: """, """failed""" ]
  Fields = [
    """(\d\d:|(\+|-))\d\d:\d\d (::ffff:)?({host}[\w\-.]+)\s""",
    """\d\d:\d\d:\d\d (::ffff:)?({host}\S+)? sshd\[""",
    """\ssshd\[\d+\]:\s*({additional_info}.+?)\s*$"""
  ]


}
```