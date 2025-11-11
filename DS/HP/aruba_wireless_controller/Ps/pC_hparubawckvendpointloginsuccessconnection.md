#### Parser Content
```Java
{
Name = hp-arubawc-kv-endpoint-login-success-connection
  Vendor = HP
  Product = Aruba Wireless controller
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,attr_name=Connection:Src-IP-Address,""", """,attr_value=""" ]
  Fields = [
    """({auth_server}({host}[A-Fa-f:\d.]+))\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),\d+\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """,session_id=({session_id}[^,]+)""",
    """,type=({auth_type}[^,]+)""",
    """,attr_name=Connection:Src-IP-Address,attr_value=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  ParserVersion = "v1.0.0"


}
```