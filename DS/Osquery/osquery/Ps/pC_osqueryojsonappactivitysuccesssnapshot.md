#### Parser Content
```Java
{
Name = osquery-o-json-app-activity-success-snapshot
  ParserVersion = "v1.0.0"
  Conditions = [ """osquery""",""""action":"snapshot"""",""""decorations":""",""""hostname":"""" ]

osquery-app-activity = {
  Vendor = Osquery
  Product = Osquery
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"calendarTime":"\w{3}\s({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d\s\w+)"""",
	""""hostname":"({host}[\w\-.]+)""""
	""""destinationServiceName":"({app}[^"]+)"""",
    """"action":"({action}[^"]+)""""
  
}
```