#### Parser Content
```Java
{
Name = unix-unix-str-process-create-success-cmd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""" CMD """,
"""]: ("""
  ]
  Fields = [
    """\w{3}\s+\d+\s+\d\d:\d\d:\d\d\s+(::ffff:)?({host}[\w\-.]+)""",
    """\(({account}[^\)]+?)\) CMD""",
    """time:"({time}\d+)""",
    """\sCMD \(\s*({process_command_line}.+?)\)($|\s|")""",
  ]
  DupFields = [ "account->user" ]


}
```