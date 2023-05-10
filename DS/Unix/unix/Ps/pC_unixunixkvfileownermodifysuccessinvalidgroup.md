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
    """\[({src_ip}[a-fA-F\d.:]+)\]\[\d+\]\[""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+)""",
    """({command}chown)""",
    """({failure_reason}invalid group): ‘([^‘’:]+):({dest_group}[^‘’:]+)’""", # target_owner is removed
  ]
  DupFields = [ "host->dest_host" ]


}
```