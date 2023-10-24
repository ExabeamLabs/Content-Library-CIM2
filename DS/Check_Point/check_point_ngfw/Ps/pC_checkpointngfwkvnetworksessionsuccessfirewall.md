#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-network-session-success-firewall
  Vendor = Check Point
  Product = Check Point NGFW
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """ProductName ="VPN-1 & FireWall-1""", """ProductFamily="Network"""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\S+\s({host}\d+.\d+.\d+.\d+)\s""",
    """src="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """proto="({protocol}[^"]+)""",
    """sport_svc="({src_port}\d+)""",
    """svc="({dest_port}\d+)""",
    """xlatedst="({dest_translated_ip}\d+.\d+.\d+.\d+)""",
    """rule_name="(?:({rule}[^"]+))"""",
    """vpn_feature_name="+({vpn_feature_name}[^"]+)"""",
    """vpn_user="+({user}[\w\.\-]{1,40}\$?)"""",
    """inzone="+({inzone}[^"]+)"""",
    """outzone="+({outzone}[^"]+)"""",
    """service_id="+({service_id}[^"]+)"""",
    """community="+(|({community}[^"]+))"+\s(\w+=|$)""",
  ]


}
```