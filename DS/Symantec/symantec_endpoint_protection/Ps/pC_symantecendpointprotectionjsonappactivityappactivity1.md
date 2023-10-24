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
    """User1:\s*({user}[\w\.\-]{1,40}\$?)\s*(,|$)""",
    """Computer:\s*({src_host}[^,]+?)\s*(,|$)""",
    """IP Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """,Category:([^,]*,){2}({event_name}[^\.]+)""",
    """LiveUpdate Manager,\s*"?({event_name}.+?)\s*"?,Event time:""",
    """,User2:[^,]*,\s*({event_name}[^\.,]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```