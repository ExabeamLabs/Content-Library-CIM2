#### Parser Content
```Java
{
Name = unix-sm-kv-email-send
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Sendmail
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [
""" msgid=""",
""" from=""",
""" nrcpts="""
  ]
  Fields = [
    """({time}\d\d\d\d-\d+-\d+T\d+:\d+:\d+\.\d+[^\s]+)"""
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?(Message|({host}[\w\-.]+))\s""",
    """(sendmail|sm-mta)\s*\[?\d+\]?[\s\-:]+({alert_id}\w+)""",
    """\s+from=<?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))""",
    """\ssize=({bytes}\d+)""",
    """\snrcpts=({num_recipients}\d+)""",
    """\smsgid=<({return_path}[^>]+)>""",
    """\sproto=({protocol}[^,]+)""",
    """from=({user}[\w\.\-\!\#\^\~]{1,40}\$?),""",
    """\srelay=(::ffff:)?({dest_host}[\w\-.]+)\s*\[(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]


}
```