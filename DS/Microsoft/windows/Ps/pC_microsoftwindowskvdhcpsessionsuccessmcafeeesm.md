#### Parser Content
```Java
{
Name = microsoft-windows-kv-dhcp-session-success-mcafeeesm
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM|""", """|272-32|""", """|Win_DHCP DNS dynamic update successful|""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """\sshost=({dest_host}[^.\s]+)""",
    """\ssrc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]
  DupFields = [ "dest_host->user" ]
  ParserVersion = "v1.0.0"


}
```