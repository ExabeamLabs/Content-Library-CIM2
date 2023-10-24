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
    """\s+from=<?({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^>\]\s"\\,\|]+\.[^\]\s"\\,\|>]+)>?,""",
    """\ssize=({bytes}\d+)""",
    """\snrcpts=({num_recipients}\d+)""",
    """\smsgid=<({return_path}[^>]+)>""",
    """\sproto=({protocol}[^,]+)""",
    """from=({user}[\w\.\-]{1,40}\$?),""",
    """\srelay=(::ffff:)?({dest_host}[\w\-.]+)\s*\[(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]


}
```