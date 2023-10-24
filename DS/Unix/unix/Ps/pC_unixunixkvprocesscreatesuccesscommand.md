#### Parser Content
```Java
{
Name = unix-unix-kv-process-create-success-command
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""; USER=""",
"""; COMMAND="""
  ]
  Fields = [
    """({time}\w+ \d+ \d\d:\d\d:\d\d)\s*:\s*({user}[\w\.\-]{1,40}\$?)\s*:""",
    """(-|({host}[\w.\-]+))\s+({user}[\w\.\-]{1,40}\$?)\s+:\s+TTY="""
    """"agent_hostname":"(::ffff:)?({host}[^"]+)"""",
    """\d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)((\.\d+)?(\+|-)\d\d:\d\d) (::ffff:)?({host}[\w.\-]+)\s""",
    """timestamp":"({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
    """; USER=({account}[^;]+?)\s*;""",
    """; COMMAND=({process_command_line}[^;]+?)\s*(;|$|")""",
    """"hostname":"({src_host}[^"]+)""""
  ]
  DupFields = [ "host->dest_host" ]


}
```