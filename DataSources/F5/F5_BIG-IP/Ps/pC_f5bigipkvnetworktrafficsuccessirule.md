#### Parser Content
```Java
{
Name = f5-bigip-kv-network-traffic-success-irule
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 BIG-IP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ type = irule,""", """,service_id = """, """,client_ip = """ ]
  Fields = [
    """service_id\s*=\s*({service_id}[^,]+)""",
    """client_ip\s*=\s*({src_ip}[A-Fa-f:\d.]+)""",
    """client_port\s*=\s*({src_port}\d+)""",
  ]


}
```