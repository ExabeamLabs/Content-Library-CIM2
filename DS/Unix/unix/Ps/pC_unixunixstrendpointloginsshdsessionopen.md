#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-login-sshdsessionopen
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """sshd[""", """]: """, """session opened""" ]
  Fields = [
    """(\d\d:|(\+|-))\d\d:\d\d (::ffff:)?({host}[\w\-.]+)\s""",
    """\d\d:\d\d:\d\d (::ffff:)?({host}\S+)? sshd\[""",
    """\ssshd\[\d+\]:\s*({additional_info}.+?)\s*$"""
  ]


}
```