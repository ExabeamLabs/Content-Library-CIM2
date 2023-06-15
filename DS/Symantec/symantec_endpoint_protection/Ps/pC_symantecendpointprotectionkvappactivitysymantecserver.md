#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-app-activity-symantecserver
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ SymantecServer: """, """,User1: """ ]
  Fields = [
    """({host}[\w\-.]+)\s+SymantecServer:""",
    """Event time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """User1:\s*({user}[^,]+?)\s*(,|$)""",
    """Computer:\s*({src_host}[^,]+?)\s*(,|$)""",
    """IP Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """,User2:[^,]*,\s*({event_name}[^\.]+)""",
  ]


}
```