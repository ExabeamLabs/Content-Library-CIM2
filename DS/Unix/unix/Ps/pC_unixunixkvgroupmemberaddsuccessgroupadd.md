#### Parser Content
```Java
{
Name = unix-unix-kv-group-member-add-success-groupadd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """][""", """ groupadd """, """ name=""" ]
  Fields = [
    """\[({src_ip}[a-fA-F\d.:]+)\]\[\d+\]\[""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) groupadd""",
    """group added to ({dest_group}[^:]+)""",
# new_group_name is removed
# new_group_id is removed
  ]
  DupFields = [ "host->dest_host", "new_group_name->group_name" ]


}
```