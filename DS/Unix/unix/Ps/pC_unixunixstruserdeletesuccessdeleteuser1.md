#### Parser Content
```Java
{
Name = unix-unix-str-user-delete-success-deleteuser-1
  Vendor = Unix
  Product = Unix
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ delete """, """ userdel[""",""" group '""" ]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)? ({host}[\w.\-]+)\suserdel""",
    """delete\s+\'({dest_user}[^']+)\'""",
    """group\s+'({group_name}[^']+)'"""
  ]
  DupFields=["host->dest_host", "dest_user->account_name"]


}
```