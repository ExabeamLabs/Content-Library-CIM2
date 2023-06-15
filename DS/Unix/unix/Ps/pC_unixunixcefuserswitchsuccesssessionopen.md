#### Parser Content
```Java
{
Name = unix-unix-cef-user-switch-success-sessionopen
  Vendor = Unix
  Product = Unix
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|Unix|Unix|""", """|session opened|""", """cs1=su """ ]
  Fields = [
    """\srt=({time}\d{13})""",
    """\sduser=({user}.+?)\s+\w+=""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdhost=({dest_host}[^\s]+)""",
    """session opened for user ({account}.+?) by""",
    """session opened for user.+?by ({user}[^(]+)""",
    """\(uid\\+=({user_uid}\d+)\)""",
    """({event_code}su)"""
  ]
  DupFields = [ "dest_host->host"]


}
```