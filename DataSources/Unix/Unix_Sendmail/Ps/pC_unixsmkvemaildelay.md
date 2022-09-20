#### Parser Content
```Java
{
Name = unix-sm-kv-email-delay
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Sendmail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
""" dsn=""",
""" delay=""",
""" relay=""",
""" stat="""
  ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?(Message|({host}[\w\-.]+))\s""",
    """\w+ \d{2} \d{2}:\d{2}:\d{2} (Message forwarded from )?(::ffff:)?({host}[\w.\-]+):? \S+ ({alert_id}\S+?):""",
    """\sstat=({result}\w+)""",
    """to=({email_recipients}<?({dest_email_address}[^@=]+@[^>,]+)[^=]*?),\s+\w+=""",
    """\srelay=({dest_host}[^\s\[]+?)\.?\s*\[({dest_ip}[a-fA-F:\d.]+)?""",
    """({bytes}\d+)\sbytes"""
  ]


}
```