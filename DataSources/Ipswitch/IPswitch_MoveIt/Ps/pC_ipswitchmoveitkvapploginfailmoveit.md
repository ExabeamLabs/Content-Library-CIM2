#### Parser Content
```Java
{
Name = ipswitch-moveit-kv-app-login-fail-moveit
  Vendor = Ipswitch
  Product = IPswitch MoveIt
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|IPswitch|MoveIt|""","""|FAILED: Sign On|""" ]
  Fields = [
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)\s\w+=""",
    """\srt=({time}\d+)""",
    """\smsg=Failed to sign on:\s({failure_reason}.+?)\sart=""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sshost=({src_host}[^\s]+)\s\w+=""",
    """requestClientApplication=({user_agent}.+?)\s\w+=""",
    """({app}MoveIt)"""
  ]


}
```