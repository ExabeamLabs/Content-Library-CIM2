#### Parser Content
```Java
{
Name = microsoft-dhcpsyslog-csv-dns-record-modify-fail-updatefail
   Vendor = Microsoft
   Product = DHCP Syslog
   ParserVersion = "v1.0.0"
   TimeFormat = "MM/dd/yy,HH:mm:ss"
   Conditions = [  """,DNS Update Failed,""" ]
   Fields = [
      """\d\d:\d\d:\d\d\s({src_host}\S+)\s[^,\s]+,""",
      """({time}\d\d/\d\d/\d\d,\d\d:\d\d:\d\d)""",
      """({event_name}DNS Update Failed)""",
      """DNS Update Failed,({dest_ip}[A-Fa-f:\d.]+)""",
      """DNS Update Failed,(([^,]+),){1}({dest_host}[^,]+)""",
      """<leaf>\S+\s+({host}[^\s<]+)\s+({src_ip}[A-Fa-f:\d.]+)"""
   ]
  DupFields = [ "dest_host->user" ]


}
```