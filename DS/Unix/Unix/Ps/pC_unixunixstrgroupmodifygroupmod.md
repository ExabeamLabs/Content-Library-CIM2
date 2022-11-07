#### Parser Content
```Java
{
Name = unix-unix-str-group-modify-groupmod
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """][""", """ groupmod """, """ group changed in """ ]
  Fields = [
    """\[({src_ip}[a-fA-F\d.:]+)\]\[\d+\]\[""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) groupmod""",
    """group changed in ({dest_group}.+?) \(group (.+?)\)""", # modified_group_name is removed
  ]
  DupFields = [ "host->dest_host" ]


}
```