#### Parser Content
```Java
{
Name = unix-sm-kv-email-delay
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Sendmail
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "MMM dd HH:mm:ss"]
  Conditions = [
""" dsn=""",
""" delay=""",
""" relay=""",
""" stat="""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?(Message|({host}[\w\-.]+))\s""",
    """\w+ \d{2} \d{2}:\d{2}:\d{2} (Message forwarded from )?(::ffff:)?({host}[\w.\-]+):? \S+ ({alert_id}\S+?):""",
    """\sstat=({result}\w+)""",
    """to=(\w+,|)<?(({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\;,\|\>]+))?""",
    """\srelay=({dest_host}[^\s\[]+?)\.?\s*\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))?""",
    """({bytes}\d+)\sbytes"""
    """(sendmail|sm-mta)\s*\[?\d+\]?[\s\-:]+({alert_id}\w+)"""
  ]


}
```