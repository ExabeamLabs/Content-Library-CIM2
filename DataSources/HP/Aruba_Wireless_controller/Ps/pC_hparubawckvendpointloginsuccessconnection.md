#### Parser Content
```Java
{
Name = hp-arubawc-kv-endpoint-login-success-connection
  Vendor = HP
  Product = Aruba Wireless controller
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,attr_name=Connection:Src-IP-Address,""", """,attr_value=""" ]
  Fields = [
    """({host}[A-Fa-f:\d.]+)\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),\d+\s({dest_ip}[A-Fa-f:\d.]+)""",
    """,session_id=({session_id}[^,]+)""",
    """,type=({auth_type}[^,]+)""",
    """,attr_name=Connection:Src-IP-Address,attr_value=({src_ip}[A-Fa-f:\d.]+)""",
  ]
  DupFields = [ "host->auth_server" ]
  ParserVersion = "v1.0.0"


}
```