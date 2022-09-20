#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-login-fail-failpass
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """][""", """ sshd """, """ Failed password for """ ]
  Fields = [
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) sshd""",
    """Failed password for.+?user (({domain}[^\\]+?)\\+)?({user}[^\\]+?) from """,
    """\sfrom ({src_ip}[a-fA-F\d.:]+)""",
    """\sport ({src_port}\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```