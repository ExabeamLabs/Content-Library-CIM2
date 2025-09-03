#### Parser Content
```Java
{
Name = cisco-sourcefire-cef-app-activity-success-router
 ParserVersion = "v1.0.0"
 Vendor = Cisco
 Product = Cisco Network Security
 TimeFormat = "epoch"
 Conditions = [ """CEF:0|CISCO|CiscoRouter|""", """agentZoneURI=""","""deviceZoneURI=""" ]
 Fields = [
   """\srt=({time}\d{13})""",
   """cs3=({event_category}[^\s]+)""",
   """cs5=({event_name}[^\s]+)""",
   """ahost=({host}[^\s]+)""",
   """dvc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
   """dtz=({country}[^\s]+)""",
   """ad.message=({additional_info}.*?)\said=""",
   ]


}
```