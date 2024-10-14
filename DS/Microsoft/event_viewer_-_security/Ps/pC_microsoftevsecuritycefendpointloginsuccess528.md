#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-login-success-528
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = [ """|Microsoft|Microsoft Windows|""", """|Security:528|""" ]
  Fields = [
    """({event_name}Successful Logon)""",
    """({event_code}528)""",
    """\srt=({time}\d{13})""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
    """\ssproc=({auth_process}.+?)\s+\w+=""",
    """\sdntdom=({domain}[^\s]+)""",
    """\sduid=\([^,]+,({login_id}[^\)]+)""",
    """\scn1=({login_type}\d+)""",
    """\sdvchost=({host}[\w\-.]+)""",
    """\sduser=(.*?\\+)?({account}.*?)\s+\w+=""",
  ]
  DupFields = [ "host->dest_host"]


}
```