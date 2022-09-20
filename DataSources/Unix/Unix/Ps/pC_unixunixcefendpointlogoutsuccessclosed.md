#### Parser Content
```Java
{
Name = unix-unix-cef-endpoint-logout-success-closed
  Product = Unix
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|Unix|Unix|""", """|session closed|""", """cs1=ssh""" ]

cef-ssh-logout = {
  Vendor = Unix
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wdvc=({host}[^\s]+)""",
    """\Wdvchost=({host}[^\s]+)""",
    """\Wsrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\Wshost=({src_host}[^\s]+)""",
    """\Wduser=({user}.+?)\s+\w+=""",
    """\Wdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\Wdhost=({dest_host}[^\s]+)""",
    """\Wcs1=({event_code}.+?)\s+(\w+=|$)"""
  
}
```