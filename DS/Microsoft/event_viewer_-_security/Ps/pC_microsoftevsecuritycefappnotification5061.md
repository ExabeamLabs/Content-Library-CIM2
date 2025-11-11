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
    """cat=({category}[^=]+)\s\w+=""",
    """dhost=({dest_host}[^=]+)\s\w+=""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
    """ahost=({host}[^=]+)\s\w+=""",
    """duser=({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+="""
  ]


}
```