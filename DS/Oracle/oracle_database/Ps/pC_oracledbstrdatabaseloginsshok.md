#### Parser Content
```Java
{
Name = oracle-db-str-database-login-sshok
  ParserVersion = v1.0.0
  Product = Oracle Database
  Vendor = Oracle
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ login - ssh ok """ ]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({event_name}login .*?)\s+session\s+({session_id}\d+)\s+by\s+({user}.+?)\s+as\s+({=user}[^:]+?):({account}.+?)\s+from\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]


}
```