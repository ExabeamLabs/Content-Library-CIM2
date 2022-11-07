#### Parser Content
```Java
{
Name = microsoft-windows-kv-dhcp-session-success-mcafeeesm
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM|""", """|272-32|""", """|Win_DHCP DNS dynamic update successful|""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\sshost=({dest_host}[^.\s]+)""",
    """\ssrc=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  ]
  DupFields = [ "dest_host->user" ]
  ParserVersion = "v1.0.0"


}
```