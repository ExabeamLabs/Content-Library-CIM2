#### Parser Content
```Java
{
Name = unix-unix-str-user-modify-usermod
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """usermod[""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s""",
    """\w{3}\s*\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[^\s]+)\s({event_code}[^:\s]+)\s*:\s*({event_name}.+?)\s*$""",
    """usermod.+?user\s'({user}[^\s']+)'""",
    """usermod[^:]+:\s({additional_info}[^:]+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```