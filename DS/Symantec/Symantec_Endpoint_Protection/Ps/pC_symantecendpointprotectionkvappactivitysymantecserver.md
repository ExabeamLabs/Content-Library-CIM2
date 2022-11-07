#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-app-activity-symantecserver
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "epoch"
  Conditions = [ """ SymantecServer: """, """,User1: """ ]
  Fields = [
    """({host}[\w\-.]+)\s+SymantecServer:""",
    """Event time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """User1:\s*({user}[^,]+?)\s*(,|$)""",
    """Computer:\s*({src_host}[^,]+?)\s*(,|$)""",
    """IP Address:\s*({src_ip}[a-fA-F\d.:])""",
    """,User2:[^,]*,\s*({event_name}[^\.]+)""",
  ]


}
```