#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-user-privilege-assign-success-576-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|Snare|""","""|Security:576|""" ]
  Fields = [
    """({event_name}Special privileges assigned to new logon)""",
    """({event_code}576)""",
    """\srt=({time}\d{13})""",
    """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
    """\sduid=\([^,]+,({login_id}[^\)]+)""",
    """\sdntdom=({domain}.+?)\s+\w+=""",
    """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
    """\sdhost=({dest_host}[\w\-.]+?)\s+\w+=""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+\w+=""",
    """\sdpriv=({privileges}.+?)\s+\w+=""",
    """\sdvchost=({host}.+?)\s+\w+=""",
    """categoryresult=\/({result}[^\s]+)""",
  ]


}
```