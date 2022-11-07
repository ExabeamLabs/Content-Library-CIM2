#### Parser Content
```Java
{
Name = cisco-sourcefire-cef-app-activity-success-router
 ParserVersion = "v1.0.0"
 Vendor = Cisco
 Product = Cisco SourceFire
 TimeFormat = "epoch"
 Conditions = [ """CEF:0|CISCO|CiscoRouter|""", """agentZoneURI=""","""deviceZoneURI=""" ]
 Fields = [
   """\srt=({time}\d+)""",
   """cs3=({event_category}[^\s]+)""",
   """cs5=({event_name}[^\s]+)""",
   """ahost=({host}[^\s]+)""",
   """dvc=({src_ip}[^\s]+)""",
   """dtz=({country}[^\s]+)""",
   """ad.message=({additional_info}.*?)\said=""",
   ]


}
```