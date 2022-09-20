#### Parser Content
```Java
{
Name = microsoft-dhcpsyslog-csv-dns-record-modify-update
   Vendor = Microsoft
   Product = DHCP Syslog
   ParserVersion = "v1.0.0"
   TimeFormat = "MM/dd/yy,HH:mm:ss"
   Conditions = [  """,DNS Update Request,""" ]
   Fields = [
      """\d\d:\d\d:\d\d\s({src_host}\S+)\s[^,\s]+,""",
      """({time}\d\d/\d\d/\d\d,\d\d:\d\d:\d\d)""",
      """({event_name}DNS Update Request)""",
      """DNS Update Request,({dest_ip}[A-Fa-f:\d.]+)""",
      """DNS Update Request,(([^,]+),){1}({dest_host}[^,]+)""",
      """<leaf>\S+\s+({host}[^\s<]+)\s+({src_ip}[A-Fa-f:\d.]+)"""
   ]
  DupFields = [ "dest_host->user" ]


}
```