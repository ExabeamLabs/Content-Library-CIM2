#### Parser Content
```Java
{
Name = unix-sm-kv-email-send
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Sendmail
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""" msgid=""",
""" from=""",
""" nrcpts="""
  ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?(Message|({host}[\w\-.]+))\s""",
    """sendmail\S*:\s+({alert_id}\S+?):\s""",
    """sm-mta\S*:\s+({alert_id}\S+?):\s""",
    """\s+from=<?({email_address}[^@=<>,]+@[^\s@=<>,]+)""",
    """\ssize=({bytes}\d+)""",
    """\snrcpts=({num_recipients}\d+)""",
    """\smsgid=<({return_path}[^>]+)>""",
    """\sproto=({protocol}[^,]+)""",
    """from=({user}[^,@\s]+),""",
    """\srelay=(::ffff:)?({dest_host}[\w\-.]+)\s*\[(::ffff:)?({dest_ip}[a-fA-F:\d.]+)""",
  ]


}
```