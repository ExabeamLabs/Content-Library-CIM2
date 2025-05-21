#### Parser Content
```Java
{
Name = oracle-db-str-app-login-fail-sshfailed
  Vendor = Oracle
  Product = Oracle Database
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ login - ssh failed """ ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """({event_name}login .*?)\s+session\s+({session_id}\d+)\s+by\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+as\s+({=user}[^:]+?):({account}.+?)\s+from\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]


}
```