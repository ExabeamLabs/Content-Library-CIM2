#### Parser Content
```Java
{
Name = unix-unix-str-user-create-fail-failedaddinguser
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """][""", """ useradd """, """ failed adding user """ ]
  Fields = [
    """\[({src_ip}[a-fA-F\d.:]+)\]\[\d+\]\[""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) useradd""",
    """failed adding user '({account_name}[^']+)'"""
    """failed adding user\s+'({user}[^"]+)'"""
  ]
  DupFields = [ "host->dest_host" ]


}
```