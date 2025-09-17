#### Parser Content
```Java
{
Name = microsoft-evsystem-json-service-state-modify-7036
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - System"
  TimeFormat = "yyyy-MM-dd HH:mm:ss Z"
  Conditions = [ """"EventID":7036""", """"Computer":""", """"Channel":"System"""" ]
  Fields = [
   """TimeCreated":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\s(\+|-)\d+)""""
   """({event_code}7036)"""
   """"Computer":"({host}[\w\-\.]+)""""
   """"Message":"({event_name}[^"]+)""""
   """"ProcessId":({process_id}\d+)"""
   """"Keywords":"({result}[^"]+)""""
   """The ({service_name}[^\.="]+) service entered the ({service_state}[^\.="]+) state"""
  ]


}
```