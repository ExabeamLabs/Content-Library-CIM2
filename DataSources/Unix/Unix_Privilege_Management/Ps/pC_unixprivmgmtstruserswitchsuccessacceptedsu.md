#### Parser Content
```Java
{
Name = unix-privmgmt-str-user-switch-success-acceptedsu
  Vendor = Unix
  Product = Unix Privilege Management
  TimeFormat = "epoch_sec"
  Conditions = [ """ upm-log end=""", """: accepted su""" ]
  Fields = [
    """({host}[\w\.\-]+)\s+upm-log end=({time}\d+)""",
    """: accepted su \S+\s+({dest_user}[^\s]+)""",
    """ from ({user}[^@\s]+)@(eth0\.)?({src_host}[^@\s]+)""",
    """ to ({dest_user}[^@\s]+)@(eth0\.)?({dest_host}[^@\s]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```