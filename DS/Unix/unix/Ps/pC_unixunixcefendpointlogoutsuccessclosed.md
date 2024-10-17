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
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}[^\s]+)""",
    """\Wdvchost=({host}[^\s]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wshost=({src_host}[^\s]+)""",
    """\Wduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdhost=({dest_host}[^\s]+)""",
    """\Wcs1=({event_code}.+?)\s+(\w+=|$)"""
  
}
```