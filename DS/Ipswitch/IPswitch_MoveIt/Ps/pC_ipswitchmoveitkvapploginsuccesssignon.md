#### Parser Content
```Java
{
Name = ipswitch-moveit-kv-app-login-success-signon
  Vendor = Ipswitch
  Product = IPswitch MoveIt
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|IPswitch|MoveIt|""","""|Sign On|""" ]
  Fields = [
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)\s\w+=""",
    """\srt=({time}\d+)""",
    """\ssuser=({account_id}.+?)\s(\w+=|$)""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sshost=({src_host}[^\s]+)\s\w+=""",
    """requestClientApplication=({user_agent}.+?)\s\w+=""",
    """({app}MoveIt)"""
  ]
   DupFields=["account_id->user"]


}
```