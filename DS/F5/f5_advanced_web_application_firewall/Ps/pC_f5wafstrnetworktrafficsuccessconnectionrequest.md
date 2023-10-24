#### Parser Content
```Java
{
Name = f5-waf-str-network-traffic-success-connectionrequest
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Advanced Web Application Firewall
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """HTTP_REQUEST:CONNECT""", """Connection Request from Client""", """VIRTUAL_SERVER:""" ]
  Fields = [
    """(?i:Date):\[({time}\d{2}\/\w{3}\/\d{4}:\d{2}:\d{2}:\d{2} (\+|-)\d{4})""",
    """\d\d:\d\d:\d\d ({host}[\w.-]+)""",
    """Client:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
    """POOL_MEMBER:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
    """SERVER_PORT:({dest_port}\d{1,5})""",
    """({event_name}Connection Request from Client)""",
    """({protocol}HTTP\/\S+?)\s"""
  ]


}
```