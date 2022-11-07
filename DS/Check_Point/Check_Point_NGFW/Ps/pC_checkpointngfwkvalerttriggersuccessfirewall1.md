#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-alert-trigger-success-firewall-1
  Vendor = Check Point
  Product = Check Point NGFW
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """ProductName ="VPN-1 & FireWall-1""", """ProductFamily="Network"""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\S+\s({host}\d+.\d+.\d+.\d+)\s""",
    """src="({src_ip}\d+.\d+.\d+.\d+)""",
    """dst="({dest_ip}\d+.\d+.\d+.\d+)""",
    """proto="({protocol}[^"]+)""",
    """sport_svc="({src_port}\d+)""",
    """svc="({dest_port}\d+)""",
    """xlatedst="({dest_translated_ip}\d+.\d+.\d+.\d+)""",
    """rule_name="(?:({rule}[^"]+))"""",
    """vpn_feature_name="+({vpn_feature_name}[^"]+)"""",
    """vpn_user="+({user}[^"]+)"""",
    """inzone="+({inzone}[^"]+)"""",
    """outzone="+({outzone}[^"]+)"""",
    """service_id="+({service_id}[^"]+)"""",
    """community="+(|({community}[^"]+))"+\s(\w+=|$)""",
  ]


}
```