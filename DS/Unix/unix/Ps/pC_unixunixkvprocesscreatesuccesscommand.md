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
    """({time}\w+ \d+ \d\d:\d\d:\d\d)\s*:\s*({user}[^:]+?)\s*:""",
    """"agent_hostname":"(::ffff:)?({host}[^"]+)"""",
    """\d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)((\.\d+)?(\+|-)\d\d:\d\d) (::ffff:)?({host}[\w.\-]+)\s""",
    """timestamp":"({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
    """; USER=({account}[^;]+?)\s*;""",
    """; COMMAND=({process_command_line}[^;]+?)\s*(;|$|")""",
    """; COMMAND=({process_path}({process_dir}[^\s]+[\\\/]+)?({process_name}[^";\\\/\s]+))[\s"](?:|;|$)""",
    """COMMAND=[^;]+;\s*({dest_process_path}({dest_process_dir}[^"]+)\/)?({dest_process_name}[^"]+)("|'|$)""",
    """"hostname":"({src_host}[^"]+)""""
    """; COMMAND=({parent_process_path}({parent_process_dir}[^,"]+[\\\/]+)?({parent_process_name}[^\s"]+))\s*"""
  ]
  DupFields = [ "host->dest_host" ]


}
```