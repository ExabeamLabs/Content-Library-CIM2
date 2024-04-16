#### Parser Content
```Java
{
Name = unix-unix-mix-endpoint-logout-sessionclosed
  Vendor = Unix
  Product = Unix
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ pam_unix""", """session closed for user """ ]
  Fields = [
    """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d (::ffff:)?({host}\S+) ({event_code}\S+)""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+(::ffff:)?({host}[\w\-.]+)\s+""",
    """({event_code}[^\s:\[]+?)(\[[^\]]*\])?:\s*pam_unix""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """(({event_name}session closed for user)\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))""",
  ]
  DupFields = [ "host->src_host" ]


}
```