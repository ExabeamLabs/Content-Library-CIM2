#### Parser Content
```Java
{
Name = cisco-tacacs-kv-process-create-success-tacacs
  Vendor = Cisco
  Product = Cisco ACS
  TimeFormat = "epoch_sec"
  Conditions = [ """[TACACS]""", """start_time=""", """cmd=""" ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+\S+\s+({user}[^\s]+)\s+\S+\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+""",
    """start_time=({time}\d{10})""",
    """cmd=\S+\s+({process_command_line}.+?)\s*$""",
    """cmd=\S+\s+({process_name}[^\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```