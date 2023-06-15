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
    """\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[\d+\]\[""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) groupmod""",
    """group changed in ({dest_group}.+?) \(group (.+?)\)""", # modified_group_name is removed
  ]
  DupFields = [ "host->dest_host" ]


}
```