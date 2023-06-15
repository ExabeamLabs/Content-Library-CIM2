#### Parser Content
```Java
{
Name = oracle-db-str-app-logout-logoutok
  ParserVersion = v1.0.0
  Vendor = Oracle
  Product = Oracle Database
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ logout ok """ ]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({event_name}logout.+?)\s+session\s+({session_id}\d+)\s+by\s+({user}.+?)\s+as\s+({=user}[^:]+?):({account}.+?)\s+from\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]


}
```