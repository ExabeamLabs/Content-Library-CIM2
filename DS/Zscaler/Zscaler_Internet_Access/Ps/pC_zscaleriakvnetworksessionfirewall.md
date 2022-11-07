#### Parser Content
```Java
{
Name = zscaler-ia-kv-network-session-firewall
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [
"""department""",
"""avgduration""",
"""locationname"""
  ]
  Fields = [
    """({time}\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """action=({action}[^\s]+)""",
    """user=(({email_address}[^@]+@[^\s]*)|({user}[^\s]+))\s""",
    """csip=({src_ip}[^\s]+)""",
    """sdip=({dest_ip}[^\s]+)""",
    """sdport=({dest_port}\d+)""",
    """csport=({src_port}\d+)""",
    """proto=({protocol}[^\s]+)""",
    """inbytes=({bytes_in}\d+)""",
    """outbytes=({bytes_out}\d+)""",
    """department=({department}[^\=]+?)\s+\w+=""",
    """locationname=({location}[^\=]+?)\s+\w+=""",
    """tsip=(0\.0\.0\.0|({tunnel_src_ip}[\da-fA-F.:]+))""",
    """tunsport=({tunnel_src_port}\d+)""",
    """tuntype=({tunnel_type}[^\s]+)""",
    """destcountry=((?i)Other|({dest_country}[^\=]+?)\s+\w+=)""",
    """nwsvc=({dest_service_name}[^\s]+)""",
    """devicehostname=(NA|({host}[^\"]+?)\s*(\w+=|\"*$))""",
    """ipcat=(Miscellaneous or Unknown|({ip_category}[^\=]+?)\s+\w+=)""",
    """deviceowner=(NA|({device_owner}[^\s]+))""",
    """rulelabel=({rule}.+?)\s*inbytes"""
]


}
```