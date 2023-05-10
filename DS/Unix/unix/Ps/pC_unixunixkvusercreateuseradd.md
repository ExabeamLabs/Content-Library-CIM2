#### Parser Content
```Java
{
Name = unix-unix-kv-user-create-useradd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """][""", """ useradd """, """ new group: """, """ GID=""" ]
  Fields = [
    """\[({src_ip}[a-fA-F\d.:]+)\]\[\d+\]\[""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) useradd""",
    """new group: name=({group_name}[^,]+),""",
    """new group: .+?GID=({group_id}\d+),""",
  ]
  DupFields = [ "host->dest_host" ]


}
```