#### Parser Content
```Java
{
Name = microsoft-dhcpsyslog-csv-dns-record-modify-update
   Vendor = Microsoft
   Product = Microsoft DHCP Log
   ParserVersion = "v1.0.0"
   TimeFormat = "MM/dd/yy,HH:mm:ss"
   Conditions = [  """,DNS Update Request,""" ]
   Fields = [
      """\d\d:\d\d:\d\d\s({src_host}[\w\-.]+)\s[^,\s]+,""",
      """"hostname":"({src_host}[\w\-.]+)",""",
      """({time}\d\d/\d\d/\d\d,\d\d:\d\d:\d\d)""",
      """({event_name}DNS Update Request)""",
      """DNS Update Request,({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """DNS Update Request,(([^,]+),){1}({dest_host}[\w\-.]+),([^,]*),(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),""",
      """<leaf>\S+\s+({host}[^\s<]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
   ]


}
```