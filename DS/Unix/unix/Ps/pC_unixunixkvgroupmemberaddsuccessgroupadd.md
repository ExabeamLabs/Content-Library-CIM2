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
    """\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[\d+\]\[""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) groupadd""",
    """group added to ({dest_group}[^:]+)""",
# new_group_name is removed
# new_group_id is removed
  ]
  DupFields = [ "host->dest_host", "new_group_name->group_name" ]


}
```