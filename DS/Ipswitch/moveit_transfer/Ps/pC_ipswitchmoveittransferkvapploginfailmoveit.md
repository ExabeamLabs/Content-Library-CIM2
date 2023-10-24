#### Parser Content
```Java
{
Name = ipswitch-moveittransfer-kv-app-login-fail-moveit
  Vendor = Ipswitch
  Product = MoveIt Transfer
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|IPswitch|MoveIt|""","""|FAILED: Sign On|""" ]
  Fields = [
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)\s\w+=""",
    """\srt=({time}\d{13})""",
    """\smsg=Failed to sign on:\s({failure_reason}.+?)\sart=""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sshost=({src_host}[^\s]+)\s\w+=""",
    """requestClientApplication=({user_agent}.+?)\s\w+=""",
    """({app}MoveIt)"""
  ]


}
```