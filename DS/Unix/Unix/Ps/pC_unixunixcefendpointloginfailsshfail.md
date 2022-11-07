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
    """\Wrt=({time}\d+)""",
    """\Wdvc=({host}[^\s]+)""",
    """\Wdvchost=({host}[^\s]+)""",
    """\Wsrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\Wshost=({src_host}[^\s]+)""",
    """\Wduser=({user}.+?)\s+\w+=""",
    """\Wdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\Wdhost=({dest_host}[^\s]+)""",
    """\Wcs4=({login_id}\d+)""",
    """CEF:([^\|]*\|){5}({failure_reason}[^\|]+)""",
    """({auth}password)""",
    """cs1=({event_code}.+?)\s+(\w+=|$)"""
  ]


}
```