#### Parser Content
```Java
{
Name = unix-privmgmt-kv-user-switch-fail-upmlog
  Vendor = Unix
  Product = Unix Privilege Management
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """ upm-log end=""", """ rejected """ ]
  Fields = [
    """({host}[\w\.\-]+)\s+upm-log end=({time}\d{10})""",
    """: rejected (({dest_user}root)|({process_name}.+?))\s+from """,
    """ from ({user}[\w\.\-]{1,40}\$?)@(eth0\.)?({src_host}[^@\s]+)""",
  ]


}
```