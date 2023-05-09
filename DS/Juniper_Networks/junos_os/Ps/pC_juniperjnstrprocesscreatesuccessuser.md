#### Parser Content
```Java
{
Name = juniper-jn-str-process-create-success-user
  ParserVersion = v1.0.0

  Conditions = [ 
"""]: UI_CMDLINE_READ_LINE: User """
""", command """
]

juniper-process-created = {
  Vendor = Juniper Networks
  Product = Junos OS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\s+\d+\s\d\d:\d\d:\d\d\s({host}[^\s]+)\s""",
    """User '({user}[^']+)'""",
    """ command '({process_command_line}[^']+?)\s*'""",
  
}
```