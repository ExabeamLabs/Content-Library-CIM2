#### Parser Content
```Java
{
Name = unix-privmgmt-str-user-switch-success-acceptedsu
  Vendor = Unix
  Product = Unix Privilege Management
  TimeFormat = "epoch_sec"
  Conditions = [ """ upm-log end=""", """: accepted su""" ]
  Fields = [
    """({host}[\w\.\-]+)\s+upm-log end=({time}\d{10})""",
    """: accepted su \S+\s+({account}[^\s]+)""",
    """ from ({user}[^@\s]+)@(eth0\.)?({src_host}[^@\s]+)""",
    """ to ({account}[^@\s]+)@(eth0\.)?({dest_host}[^@\s]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```