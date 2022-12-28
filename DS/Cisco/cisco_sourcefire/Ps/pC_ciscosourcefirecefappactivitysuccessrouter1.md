#### Parser Content
```Java
{
Name = cisco-sourcefire-cef-app-activity-success-router-1
 ParserVersion = "v1.0.0"
 Vendor = Cisco
 Product = Cisco SourceFire
 TimeFormat = "epoch"
 Conditions = [ """CEF:0""", """|CISCO\|CiscoRouter]""", """agentZoneURI=""","""deviceZoneURI=""" ]
 Fields = [
   """\srt=({time}\d{13})""",
   """CEF:0\|([^\|]+\|){7}.*?-\s*({event_name}[^\)]+\))""",
   """ahost=({host}[^\s]+)""",
   """dvc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
   """dtz=({country}[^\s]+)""",
   ]


}
```