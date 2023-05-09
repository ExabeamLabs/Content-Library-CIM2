#### Parser Content
```Java
{
Name = pan-ngfw-cef-alert-trigger-success-threat
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "MMM dd yyyy HH:mm:ss z"
  Conditions = [ """ CEF: """, """|Palo Alto Networks|PAN-OS|""", """|THREAT|""", """PanOSThreatCategory=""", """PanOSURLCatList=""" ]
  Fields = [
    """\sdvchost=({host}[\w\-.]+)""",
    """\|rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\s\w{3})\s\w+=""",
    """({event_category}THREAT)"""
    """\|THREAT\|(Unknown|({alert_severity}[^\|]+))""",
    """\|({alert_name}[^\|]+?)((\s\(generic)?:[^\(]+)?(\(({alert_id}\d+)\))?\|THREAT\|""",
    """\scat=({alert_type}[^=]+)\s+(\w+=|$)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+(\w+=|$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+(\w+=|$)""",
    """\sspt=({src_port}\d{1,5})\s""",
    """\sdpt=({dest_port}\d{1,5})\s""",
    """\sapp=({network_app}[^=]+)\s+(\w+=|$)""",
    """\sact=({action}[^=]+?)\s\w+=""",
    """request="({malware_url}[^"]+)"""",
    """\scs2=({category}[^=]+?)\s\w+=""",
    """flexString2=({direction}[^=]+?)\s\w+=""",
    """\scs1=({rule}[^=]+?)\s\w+=""",
    """\scs4=({src_network_zone}[^=]+?)\s\w+=""",
    """\scs5=({dest_network_zone}[^=]+?)\s\w+=""",
    """PanOSThreatCategory=(unknown|({threat_category}[^=]+?))\s\w+=""",
    """\sproto=({protocol}[^=]+?)\s\w+=""",
    """sourceTranslatedAddress=({src_translated_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
    """destinationTranslatedAddress=({dest_translated_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
  ]
  ParserVersion = "v1.0.0"


}
```