#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-app-notification-eventdescription
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "epoch"
  Conditions = [ """ SymantecServer: """, """,Event Description: """ ]
  Fields = [
    """({host}[\w\-.]+)\s+SymantecServer:""",
    """Event time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """Category:\s*({category}[^,]+)""",
    """Event Description:\s*({event_name}[^,]+?)\.?\s*(,|$)"""
  ]


}
```