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
    """\s\d{1,2}\s\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?sudo"""
    """({time}\d\d\s\w\w\w\s\d\d\d\d\s\d\d:\d\d:\d\d)"""
    """; USER=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*;""",
    """({time}\w+ \d+ \d\d:\d\d:\d\d)\s*:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*:""",
    """(-|({src_host}[\w.\-]+))\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+:\s+(user|\w+=)"""
    """"agent_hostname":"(::ffff:)?({host}[^"]+)"""",
    """\w+ \d\d \d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)((\.\d+)?(\+|-)\d\d:\d\d) (::ffff:)?({host}[\w.\-]+)\s""",
    """timestamp":"({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
    """; USER=({account}[^;]+?)\s*;""",
    """; COMMAND=({process_command_line}[^;]+?)\s*(;|$|")""",
    """"hostname":"({src_host}[^"]+)""""
    """({error_code}user NOT in sudoers)""",
    """\WPWD\\?=({current_working_dir}[^\s;=]+?)[\s;]*\w+="""
    """\WCOMMAND\\?=({process_relative_path}({process_relative_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  DupFields = [ "host->dest_host" ]


}
```