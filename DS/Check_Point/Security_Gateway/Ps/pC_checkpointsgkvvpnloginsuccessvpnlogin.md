#### Parser Content
```Java
{
Name = checkpoint-sg-kv-vpn-login-success-vpnlogin
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Security Gateway
  TimeFormat = "ddMMMyyyy-HH:mm:ss"
  Conditions = [ """product=VPN-1 & FireWall-1""", """['vpn_feature_name': """, """['origin_sic_name': """ ]
  Fields = [
    """Time:\s*({time}\d\d\w+\d\d\d\d-\d\d:\d\d:\d\d)""",
    """'user':\s*"({user}[^"]+)""",
    """'origin_sic_name':\s*"(CN=)?({host}[^",]+)""",
    """Direction:\s*({direction}\w+)\s+Connection""",
    """Action:\s*(|({action}.+?))\s*OriginSicName:""",
    """'src':\s*({src_ip}[a-fA-F\d.:]+)""",
    """'dst':\s*({dest_ip}[a-fA-F\d.:]+)""",
    """'s_port':\s*({src_port}\d+)""",
    """'service':\s*({dest_port}\d+)""",
  ]


}
```