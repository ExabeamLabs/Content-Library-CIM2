#### Parser Content
```Java
{
Name = microsoft-windows-cef-user-privilege-assign-success-576-1
  Vendor = Microsoft
  Product = Windows
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|Snare|""","""|Security:576|""" ]
  Fields = [
    """({event_name}Special privileges assigned to new logon)""",
    """({event_code}576)""",
    """\srt=({time}\d+)""",
    """\ssuser=({user}.+?)\s+\w+=""",
    """\sduid=\([^,]+,({login_id}[^\)]+)""",
    """\sdntdom=({domain}.+?)\s+\w+=""",
    """\sduser=({user}.+?)\s+\w+=""",
    """\sdhost=({dest_host}.+?)\s+\w+=""",
    """\sdst=({dest_ip}.+?)\s+\w+=""",
    """\sdpriv=({privileges}.+?)\s+\w+=""",
    """\sdvchost=({host}.+?)\s+\w+=""",
    """categoryresult=\/({result}[^\s]+)""",
  ]


}
```