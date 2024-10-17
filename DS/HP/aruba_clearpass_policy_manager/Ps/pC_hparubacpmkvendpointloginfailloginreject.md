#### Parser Content
```Java
{
Name = hp-arubacpm-kv-endpoint-login-fail-loginreject
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Common.Username=""", """Auth-Method=""", """Common.Login-Status=REJECT""", """Authentication failed""" ]
  Fields = [
    """\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2},\d+\s+({host}[\w.-]+)\s+""",
    """Timestamp=({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})((\+|\-)\d+)?""",
    """Common\.Username=({user}[\w\.\-\!\#\^\~]{1,40}\$?),""",
    """Common\.NAS-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Auth-Method=({auth_method}[^,]+),""",
    """Common.NAS-Name =({dest_host}[\w.-]+),""",
    """({event_name}Authentication failed)""",
    """Common\.Alerts=[^~]+?:\s*({failure_reason}[^:]+?)\.[^:]*MSCHAP: Authentication failed""",
    """Common\.Service=({app}[^,]+),"""
  ]


}
```