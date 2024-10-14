#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-ds-object-modify-success-5136
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = ["""|Microsoft|Microsoft Windows|""", """Microsoft-Windows-Security-Auditing:5136"""]
  Fields = [
    """({event_name}A directory service object was modified)""",
    """({event_code}5136)""",
    """\srt=({time}\d{13})""",
    """\sdvchost=({host}[^\s]+)""",
    """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
    """dhost=({dest_host}[\w\-.]+)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
    """dntdom=({domain}[^\s]+)""",
    """fileType=({ds_object_type}[^=]+)\s\w+=""",
    """cs5=({ds_object_class}[^=]+)\s\w+=""",
    """cs6=({ds_object_dn}.+?)\s\w+="""
  ]


}
```