#### Parser Content
```Java
{
Name = microsoft-windows-kv-dhcp-session-success-renew
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "epoch"
  Conditions = [ """Description=Renew""", """Host Name =""", """QResult=""" ]
  Fields = [
    """<.*?>\w+ \d+ \d+:\d+:\d+\s+({host}[^\s]+)""",
    """\sIP Address=({dest_ip}[a-fA-F\d.:]+)""",
    """\sHost Name =({dest_host}[\w.\-]+)""",
  ]
  DupFields = [ "dest_host->user" ]


}
```