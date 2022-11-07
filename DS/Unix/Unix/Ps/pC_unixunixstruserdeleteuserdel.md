#### Parser Content
```Java
{
Name = unix-unix-str-user-delete-userdel
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """][""", """ userdel """, """ removed """, """ group """, """ owned by """ ]
  Fields = [
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) userdel""",
    """removed.+?group '({group_name}[^']+)' owned by '({account_name}[^"]+)'""",
  ]
  DupFields=["host->dest_host"]


}
```