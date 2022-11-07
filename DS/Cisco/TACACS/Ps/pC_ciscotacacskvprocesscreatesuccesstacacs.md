#### Parser Content
```Java
{
Name = cisco-tacacs-kv-process-create-success-tacacs
  Vendor = Cisco
  Product = TACACS
  TimeFormat = "epoch_sec"
  Conditions = [ """[TACACS]""", """start_time=""", """cmd=""" ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+\S+\s+({user}[^\s]+)\s+\S+\s+({src_ip}[A-Fa-f:\d.]+)\s+""",
    """start_time=({time}\d+)""",
    """cmd=\S+\s+({process_command_line}.+?)\s+$""",
    """cmd=\S+\s+({process_name}[^\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```