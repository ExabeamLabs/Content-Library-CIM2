#### Parser Content
```Java
{
Name = hp-arubawc-kv-endpoint-login-success-authentication
  Vendor = HP
  Product = Aruba Wireless controller
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,attr_name=Authentication:Full-Username,""", """,attr_value=""" ]
  Fields = [
    """({host}[A-Fa-f:\d.]+)\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),\d+\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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