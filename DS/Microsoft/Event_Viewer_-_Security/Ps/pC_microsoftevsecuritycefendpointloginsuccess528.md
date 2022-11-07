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
    """\srt=({time}\d+)""",
    """\ssrc=({src_ip}[a-fA-F:\d.]+)""",
    """\ssuser=({user}.+?)\s+\w+=""",
    """\ssproc=({auth_process}.+?)\s+\w+=""",
    """\sdntdom=({domain}[^\s]+)""",
    """\sduid=\([^,]+,({login_id}[^\)]+)""",
    """\scn1=({login_type}\d+)""",
    """\sdvchost=({host}[^\s]+)""",
    """\sduser=(.*?\\+)?({account}.*?)\s+\w+=""",
  ]
  DupFields = [ "host->dest_host"]


}
```