#### Parser Content
```Java
{
Name = unix-unix-cef-endpoint-login-fail-sshfail
  Vendor = Unix
  Product = Unix
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|Unix|Unix|""", """categoryOutcome=/Failure""", """cs1=ssh""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}[^\s]+)""",
    """\Wdvchost=({host}[^\s]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wshost=({src_host}[^\s]+)""",
    """\Wduser=({user}[\w\.\-]{1,40}\$?)\s+\w+=""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdhost=({dest_host}[^\s]+)""",
    """\Wcs4=({login_id}\d+)""",
    """CEF:([^\|]*\|){5}({failure_reason}[^\|]+)""",
    """({auth}password)""",
    """cs1=({event_code}.+?)\s+(\w+=|$)"""
  ]


}
```