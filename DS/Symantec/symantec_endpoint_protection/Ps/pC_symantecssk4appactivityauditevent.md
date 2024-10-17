#### Parser Content
```Java
{
Name = symantec-s-sk4-app-activity-auditevent
    Vendor = Symantec
    Product = Symantec Endpoint Protection
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """SymantecServer""", """|audit-event|""" ]
    Fields = [
      """Event time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
      """\WrequestClientApplication=({app}[^=]+?)\s+(\w+=|$)""",
      """([^\|]*\|){5}({operation}[^\|]+)""",
      """\WdestinationServiceName =({event_subtype}.+?)\s+(\w+=|$)""",
      """({host}[\w.\-]+)\s+SymantecServer:\s*({src_host}[^,]+)(,|\s*$)""",
      """Category: \d+,[^,]+,({event_name}[^,]+)(,|\s*$)""",
    ]
    DupFields = [ "host->dest_host" ]
        ParserVersion = "v1.0.0"


}
```