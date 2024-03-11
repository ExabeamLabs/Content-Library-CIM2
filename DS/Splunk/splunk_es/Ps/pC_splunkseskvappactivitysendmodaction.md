#### Parser Content
```Java
{
Name = splunk-ses-kv-app-activity-sendmodaction
  Vendor = Splunk
  Product = Splunk ES
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ sendmodaction - """, """ signature="""", """ search_name="""", """ action_mode="""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """worker="({host}[\w\-.]+)"""",
# search_name is removed
    """signature="({signature}[^"]+)"""",
    """action_name="({action}[^"]+)"""",
    """sid="({user_sid}[^"]+)"""",
# rid is removed
    """app="({app}[^"]+)"""",
    """user="({user}[^"]+)"""",
   ]


}
```