#### Parser Content
```Java
{
Name = symantec-endpointprotection-json-app-activity-appactivity-1
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ SymantecServer: """, """,Event time: """ ]
  Fields = [
    """({host}[\w\-.]+)\s+SymantecServer:""",
    """Event time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """Category:\s*({category}[^,]+)""",
    """User1:\s*({user}[^,]+?)\s*(,|$)""",
    """Computer:\s*({src_host}[^,]+?)\s*(,|$)""",
    """IP Address:\s*({src_ip}[a-fA-F\d.:]+)""",
    """,Category:([^,]*,){2}({event_name}[^\.]+)""",
    """LiveUpdate Manager,\s*"?({event_name}.+?)\s*"?,Event time:""",
    """,User2:[^,]*,\s*({event_name}[^\.,]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```