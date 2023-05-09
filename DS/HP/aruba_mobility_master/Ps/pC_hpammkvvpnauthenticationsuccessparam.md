#### Parser Content
```Java
{
Name = hp-amm-kv-vpn-authentication-success-param
  Vendor = HP
  Product = Aruba Mobility Master
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """params:""", """mgmtd["""]
  Fields = [
    """(\w{1,3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+))""",
    """params:({additional_info}[^:]+?)\s*$""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """mgmtd([^\s]+\s){2}({event_name}[^:]+?)\sparams:""",
  ]


}
```