#### Parser Content
```Java
{
Name = microsoft-windows-kv-dhcp-session-success-dnsupdate
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "epoch"
  Conditions = [ """Description=DNS Update Successful""", """Host Name =""", """QResult=""" ]
  Fields = [
    """<.*?>\w+ \d+ \d+:\d+:\d+\s+({host}[^\s]+)""",
    """\sIP Address=({dest_ip}[a-fA-F\d.:]+)""",
    """\sHost Name =({dest_host}[\w.\-]+)""",
  ]
  DupFields = [ "dest_host->user" ]


}
```