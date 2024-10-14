#### Parser Content
```Java
{
Name = juniper-jn-str-process-create-success-client
  ParserVersion= v1.0.0
  Conditions = [ 
"""]: UI_JUNOSCRIPT_CMD: User """
""" client to run command """
]

juniper-process-created = {
  Vendor = Juniper Networks
  Product = Junos OS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\s+\d+\s\d\d:\d\d:\d\d\s({host}[^\s]+)\s""",
    """User '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """ command '({process_command_line}[^']+?)\s*'""",
  
}
```