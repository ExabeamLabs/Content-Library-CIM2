#### Parser Content
```Java
{
Name = oracle-o-str-app-logout-logoutok
  ParserVersion = v1.0.0
  Product = Oracle
  Vendor = Oracle
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ logout ok """ ]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({event_name}logout.+?)\s+session\s+({session_id}\d+)\s+by\s+({user}.+?)\s+as\s+({=user}[^:]+?):({account}.+?)\s+from\s+({src_ip}[a-fA-F\d.:]+)""",
  ]


}
```