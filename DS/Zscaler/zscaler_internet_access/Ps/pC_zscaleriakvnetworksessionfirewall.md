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
    """action=({result}[^\s]+)""",
    """user=((\w+[^=]+\->\w+[^=]+)|({email_address}[^@]+@[^\s]*)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """csip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """sdip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """sdport=({dest_port}\d+)""",
    """csport=({src_port}\d+)""",
    """proto=({protocol}[^\s]+)""",
    """inbytes=({bytes_in}\d+)""",
    """outbytes=({bytes_out}\d+)""",
    """department=({department}[^\=]+?)\s+\w+=""",
    """locationname=({location}[^\=]+?)\s+\w+=""",
    """tsip=(0\.0\.0\.0|({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))""",
    """tunsport=({src_translated_port}\d+)""",
    """tuntype=({vpn_client_type}[^\s]+)""",
    """destcountry=((?i)Other|({dest_country}[^\=]+?)\s+\w+=)""",
    """nwsvc=({dest_service_name}[^\s]+)""",
    """devicehostname=(NA|({host}[^\"]+?)\s*(\w+=|\"*$))""",
    """ipcat=(Miscellaneous or Unknown|({category}[^\=]+?)\s+\w+=)""",
    """rulelabel=({rule}.+?)\s*inbytes""",
    """\snwapp=({network_app}[^=]+?)\s+\w+=""",
    """\sthreatcat=(None|({threat_category}[^=]+?))\s+\w+=""",
    """\sthreatname=(None|({alert_name}[^=]+?))\s+\w+=""",
    """\sduration=({duration}\d+)\s+\w+=""",
    """\sdeviceowner=(None|NA|({owner_id}[^=]+?))\s+\w+="""
]
DupFields = [ "result->action" ]


}
```