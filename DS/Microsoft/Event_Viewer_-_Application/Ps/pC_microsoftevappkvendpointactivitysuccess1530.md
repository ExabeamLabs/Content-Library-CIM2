#### Parser Content
```Java
{
Name = microsoft-evapp-kv-endpoint-activity-success-1530
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Application
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""eventid="""", """eventrecordid="""", """providername=""""]
  Fields = [
     """eventid="({event_code}\d+)"*\s*task=""",
     """\d\d:\d\d:\d\d.\dZ\s+({host}[^\s]+)\s+""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
     """userid="(NT AUTHORITY|({user}.+?))\\+(SYSTEM|({domain}[^"\s]+))""",
     """providername="[^"]+"(\s+\w+="[^"]+")*\]\s+({additional_info}.+?)(\.\s|\s*"*$)""",
     """eventrecordid="({event_id}[^"]+)""",
     """providername="({provider_name}[^"]+)""",
     """channel="({channel}[^"]+)""",
     """level="({severity}[^"]+)""",
     """eventsourcename="({log_source}[^"]+)""",
  ]


}
```