#### Parser Content
```Java
{
Name = unix-unix-kv-file-owner-modify-success-invalidgroup
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """][""", """ chown""", """invalid group:""" ]
  Fields = [
    """\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[\d+\]\[""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+)""",
    """({command}chown)""",
    """({failure_reason}invalid group): ‘([^‘’:]+):({dest_group}[^‘’:]+)’""", # target_owner is removed
  ]
  DupFields = [ "host->dest_host" ]


}
```