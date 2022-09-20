#### Parser Content
```Java
{
Name = oracle-o-str-app-login-fail-sshfailed
  Product = Oracle
  Vendor = Oracle
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ login - ssh failed """ ]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({event_name}login .*?)\s+session\s+({session_id}\d+)\s+by\s+({user}.+?)\s+as\s+({=user}[^:]+?):({account}.+?)\s+from\s+({src_ip}[a-fA-F\d.:]+)""",
  ]


}
```