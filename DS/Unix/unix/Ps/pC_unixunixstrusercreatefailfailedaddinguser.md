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
    """\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[\d+\]\[""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) useradd""",
    """failed adding user '({account_name}[^']+)'"""
    """failed adding user\s+'({user}[^"]+)'"""
  ]
  DupFields = [ "host->dest_host" ]


}
```