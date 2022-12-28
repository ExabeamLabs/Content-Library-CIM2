#### Parser Content
```Java
{
Name = unix-unix-str-process-create-success-executed
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""The privilege command""",
"""is executed by"""
  ]
  Fields = [
    """Message forwarded from (::ffff:)?({host}[^\s:]+)""",
    """The privilege command ({process_command_line}({process_path}({process_dir}.+?)({process_name}[^\/]+?))), is executed"""
    """executed by user with id ({user_id}\d+)"""
  ]


}
```