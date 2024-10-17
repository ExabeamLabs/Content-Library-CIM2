#### Parser Content
```Java
{
Name = symantec-endpointprotection-json-app-activity-appactivity
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ SymantecServer: Site: """, """,Server: """ ]
  Fields = [
    """({host}[\w\-.]+)\s+SymantecServer:""",
    """SymantecServer:([^,]*,){2}({event_name}[^\.,]+?)\s*(<|$)""",
    """,Domain:\s*({web_domain}[^,]+?),Admin:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?),({event_name}.+?)\s*(<|$)""",
    """,Domain:\s*({web_domain}[^,\s]+),\s*({event_name}[^,]+),[^,]*,(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),""",
  ]
  ParserVersion = "v1.0.0"


}
```