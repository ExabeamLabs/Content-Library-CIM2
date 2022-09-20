#### Parser Content
```Java
{
Name = netskope-sc-json-network-traffic-traffictype
  ParserVersion = "v1.0.0"
  Vendor = "Netskope"
  Product = "Netskope Security Cloud"
  TimeFormat = "epoch_sec"
  Conditions = [ 
""""bypass_traffic":"""
""""traffic_type":"""
""""userkey":""" 
]
  Fields = [
    """\"+bypass_reason\"+:\s*\"+({action}[^\",]+)""",
    """\"+url\"+:\s*\"+({domain}[^\",]+)""",
    """\"user\"+:\s*\"+(({email_address}[^@]+@[^\",]+)|({user}[^\",]+))""",
    """\"+dstport\"+:\s*({dest_port}\d+)""",
    """\"hostname\"+:\s*\"+({host}[^\",]+)""",
    """\"+appcategory\"+:\s*\"+({category}[^\",]+)""",
    """\"timestamp\"+:\s*({time}\d+)""",
    """\"+src_location\"+:\s*\"+({location_city}[^\",]+)""",
    """\"+bypass_traffic\"+:\s*\"+({result}[^\",]+)""",
    """\"+userip\"+:\s*\"+({src_ip}[^\",]+)""",
    """\"+src_country\"+:\s*\"+({country_code}[^\",]+)""",
    """\"srcip\":\s*\"({src_translated_ip}[A-Fa-f:\d.]+)\"""",
    """\"+dstip\"+:\s*\"+({dest_ip}[^\",]+)""",
    """\"policy\": \"({alert_name}[^\",]+)""",
    """\"+browser\"+:\s*\"+({browser}[^\",]+)""",
    """\"+useragent\"+:\s*\"+({user_agent}[^\"]+)"""
  ]


}
```