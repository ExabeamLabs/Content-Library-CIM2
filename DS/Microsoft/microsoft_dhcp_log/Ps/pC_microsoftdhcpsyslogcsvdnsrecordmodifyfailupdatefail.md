#### Parser Content
```Java
{
Name = microsoft-dhcpsyslog-csv-dns-record-modify-fail-updatefail
   Vendor = Microsoft
   Product = Microsoft DHCP Log
   ParserVersion = "v1.0.0"
   TimeFormat = "MM/dd/yy,HH:mm:ss"
   Conditions = [  """,DNS Update Failed,""" ]
   Fields = [
      """\d\d:\d\d:\d\d\s({src_host}\S+)\s[^,\s]+,([^,]+,){2}DNS Update Failed,""",
      """"hostname":"({src_host}[^"]+)"""
      """({time}\d\d/\d\d/\d\d,\d\d:\d\d:\d\d)""",
      """({event_name}DNS Update Failed)""",
      """DNS Update Failed,(([^,]+),){1}({dest_host}[\w\-.]+)""",
      """<leaf>\S+\s+({host}[^\s<]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """DNS Update Failed,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
   ]
  


}
```