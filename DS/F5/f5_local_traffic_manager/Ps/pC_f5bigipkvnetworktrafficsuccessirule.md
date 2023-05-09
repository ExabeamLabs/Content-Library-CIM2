#### Parser Content
```Java
{
Name = f5-bigip-kv-network-traffic-success-irule
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Local Traffic Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ type = irule,""", """,service_id = """, """,client_ip = """ ]
  Fields = [
    """service_id\s*=\s*({service_id}[^,]+)""",
    """client_ip\s*=\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """client_port\s*=\s*({src_port}\d+)""",
  ]


}
```