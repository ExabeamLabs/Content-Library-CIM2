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
    """Failed password for.+?user (({domain}[^\\]+?)\\+)?({user}[\w\.\-]{1,40}\$?) from """,
    """\sfrom ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sport ({src_port}\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```