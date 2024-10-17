#### Parser Content
```Java
{
Name = unix-unix-str-user-modify-usermod
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """usermod[""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s""",
    """\w{3}\s*\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[^\s]+)\s({event_code}[^:\s]+)\s*:\s*({event_name}.+?)\s*$""",
    """usermod.+?user\s'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """usermod[^:]+:\s({additional_info}[^:]+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```