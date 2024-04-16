#### Parser Content
```Java
{
Name = unix-unix-kv-process-create-success-command
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "MMM dd HH:mm:ss", "dd MMM yyyy HH:mm:ss"]
  Conditions = [
"""; USER=""",
"""; COMMAND="""
  ]
  Fields = [
    """({time}\d\d\s\w\w\w\s\d\d\d\d\s\d\d:\d\d:\d\d)"""
    """({time}\w+ \d+ \d\d:\d\d:\d\d)\s*:\s*({user}[\w\.\-]{1,40}\$?)\s*:""",
    """(-|({src_host}[\w.\-]+))\s+({user}[\w\.\-]{1,40}\$?)\s+:\s+"""
    """"agent_hostname":"(::ffff:)?({host}[^"]+)"""",
    """\w+ \d\d \d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)((\.\d+)?(\+|-)\d\d:\d\d) (::ffff:)?({host}[\w.\-]+)\s""",
    """timestamp":"({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
    """; USER=({account}[^;]+?)\s*;""",
    """; COMMAND=({process_command_line}[^;]+?)\s*(;|$|")""",
    """"hostname":"({src_host}[^"]+)""""
    """({error_code}user NOT in sudoers)""",
    """\WPWD\\?=({process_dir}[^\s;=]+?)[\s;]*\w+="""
  ]
  DupFields = [ "host->dest_host" ]


}
```