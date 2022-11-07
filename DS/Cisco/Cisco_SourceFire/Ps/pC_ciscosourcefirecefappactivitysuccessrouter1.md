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
   """\srt=({time}\d+)""",
   """CEF:0\|([^\|]+\|){7}.*?-\s*({event_name}[^\)]+\))""",
   """ahost=({host}[^\s]+)""",
   """dvc=({src_ip}[^\s]+)""",
   """dtz=({country}[^\s]+)""",
   ]


}
```