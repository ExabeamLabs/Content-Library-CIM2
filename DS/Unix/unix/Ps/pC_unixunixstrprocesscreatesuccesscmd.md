#### Parser Content
```Java
{
Name = unix-unix-str-process-create-success-cmd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """ CMD """, """]: """ ]
  Fields = [
    """({time}\w{3}\s+\d+\s+\d\d:\d\d:\d\d)\s+(::ffff:)?({host}[\w\-.]+)""",
    """\(({account}[^\)]+?)\) CMD""",
    """time:"({time}\d+)""",
    """\sCMD \(\s*({process_command_line}.+?)\)($|\s|")""",
    """\sCMD\s+\=?\s*({process_command_line}.+?)$"""
    """CMD = ({process_command_line}[^;]+?)\s*(;|$|")"""
    """PWD = ({process_dir}[^\s,=;]+)"""
    """USER = ({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """from_remote_host = ({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """\WCMD\s+({process_path}({process_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s=]+))\s(?:|;|$)"""
  ]
  DupFields = [ "account->user" ]


}
```