#### Parser Content
```Java
{
Name = checkpoint-sg-kv-vpn-login-success-vpnlogin
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point Security Gateway
  TimeFormat = "ddMMMyyyy-HH:mm:ss"
  Conditions = [ """product=VPN-1 & FireWall-1""", """['vpn_feature_name': """, """['origin_sic_name': """ ]
  Fields = [
    """Time:\s*({time}\d\d\w+\d\d\d\d-\d\d:\d\d:\d\d)""",
    """'user':\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """'origin_sic_name':\s*"(CN=)?({host}[^",]+)""",
    """Direction:\s*({direction}\w+)\s+Connection""",
    """Action:\s*(|({action}.+?))\s*OriginSicName:""",
    """'src':\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """'dst':\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """'s_port':\s*({src_port}\d+)""",
    """'service':\s*({dest_port}\d+)""",
  ]


}
```