#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-app-notification-5061
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """|Microsoft-Windows-Security-Auditing:5061|""", """|Cryptographic operation.|""", """duser=""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """({event_name}Cryptographic operation)""",
    """({event_code}5061)""",
    """\scat=({category}[^=]+)\s\w+=""",
    """\sdhost=({dest_host}[^=]+)\s\w+=""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
    """\sahost=({host}[^=]+)\s\w+=""",
    """\sduser=({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+="""
  ]


}
```