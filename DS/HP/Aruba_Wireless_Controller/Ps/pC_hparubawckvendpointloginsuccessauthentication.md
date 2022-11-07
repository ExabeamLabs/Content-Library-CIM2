#### Parser Content
```Java
{
Name = hp-arubawc-kv-endpoint-login-success-authentication
  Vendor = HP
  Product = Aruba Wireless Controller
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,attr_name=Authentication:Full-Username,""", """,attr_value=""" ]
  Fields = [
    """({host}[A-Fa-f:\d.]+)\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),\d+\s({dest_ip}[A-Fa-f:\d.]+)""",
    """,session_id=({session_id}[^,]+)""",
    """,type=({auth_type}[^,]+)""",
    """,attr_name=Authentication:Full-Username,attr_value=({user}[^,\s@\\\/]+),""",
    """,attr_name=Authentication:Full-Username,attr_value=({full_name}[^,\s@]+)@({domain}[^,@]+)""",
    """,attr_name=Authentication:Full-Username,attr_value=(host/|(({domain}[^,\\\/]+)[\\\/]+)({full_name}[^,\s@]+))""",
  ]
  DupFields = [ "host->auth_server", "full_name->user" ]
   ParserVersion = "v1.0.0"


}
```