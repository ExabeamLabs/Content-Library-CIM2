#### Parser Content
```Java
{
Name = osquery-o-json-app-activity-success-added
  ParserVersion = "v1.0.0"
  Conditions = [ """"calendarTime":""",""""action":"added"""",""""decorations":""",""""hostname":"""" ]

osquery-app-activity = {
  Vendor = Osquery
  Product = Osquery
  TimeFormat = "MMM dd HH:mm:ss yyyy 'UTC'"
  Fields = [
    """"calendarTime":"\w{3}\s({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d\s\w+)"""",
	""""hostname":"({host}[\w\-.]+)""""
	""""destinationServiceName":"({app}[^"]+)"""",
    """"action":"({action}[^"]+)"""",
    """"uid":"({user_id}\d+)"""",
    """"protocol":"({protocol}[^"]+)"""",
    """"cmdline":"({process_command_line}[^"]+)"""",
    """destinationServiceName.+?"name":"({additional_info}[^"]+)""""
  
}
```