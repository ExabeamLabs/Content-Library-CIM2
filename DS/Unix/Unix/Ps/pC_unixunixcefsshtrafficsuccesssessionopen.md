#### Parser Content
```Java
{
Name = unix-unix-cef-ssh-traffic-success-sessionopen
  Vendor = Unix
  Product = Unix
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|session opened|""", """cs1=ssh""" ]
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wdvchost=({host}.+?)\s+(\w+=|$)""",
    """\Wsuid=({account_id}.+?)\s+(\w+=|$)""",
    """\Wduser=({user}.+?)\s+(\w+=|$)""",
    """\Wcs1=({event_code}.+?)\s+(\w+=|$)""",
    """\Wdhost=({dest_host}.+?)\s+(\w+=|$)""",
    """\Wcs4=({login_id}\d+)""",
  ]


}
```