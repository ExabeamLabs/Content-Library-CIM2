#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-app-notification-eventdescription
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """ SymantecServer: """, """,Event Description: """ ]
  Fields = [
    """(<({alert_severity}({priority}\d+))>)?({time}\w+\s\d+\s\d+:\d+:\d+)?\s*({host}[\w\-.]+)\s+SymantecServer:""",
    """Event time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """Category:\s*({category}[^,]+)""",
    """Event Description:\s*({event_name}[^,]+?)\.?\s*(,|$)"""
  ]


}
```