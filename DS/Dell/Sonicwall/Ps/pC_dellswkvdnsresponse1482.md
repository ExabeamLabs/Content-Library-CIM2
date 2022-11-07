#### Parser Content
```Java
{
Name = dell-sw-kv-dns-response-1482
  Product = Sonicwall
  ParserVersion = "v1.0.0"
  Conditions = [ """ m=1482 """, """id=""", """ fw=""", """ c=""", """ pri="""]
  Fields = ${SonicwallParsersTemplates.sonicwall-firewall.Fields} [
    """Domain:\s*({query}[^"]+)"""
  ]

sonicwall-firewall = {
  Vendor = Dell
  Product = Sonicwall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """usr="\s*(({email_address}[^@"]+@[^\\\s"]+)|({user}[^\\\s"]+))""",
    """\smsg="({additional_info}[^"]+?)\s*"""",
    """\sc=({category_id}\d+)""",
    """\sm=({message_id}\d+)""",
    """\sipscat="({category}[^"]+)""",
    """\sipspri=({alert_severity}\d+)""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({src_port}\d+))?(:({src_interface}[^\s:]+))?(:[^\s:]+)?""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({dest_port}\d+))?(:({dest_interface}[^\s:]+))?(:[^\s:]+)?""",
    """\ssrcMac=({src_mac}[a-fA-F\d.:]+)""",
    """\sdstMac=({dest_mac}[a-fA-F\d.:]+)""",
    """\sproto=({protocol}[^\s\/\d"]+)""",
    """\srcvd=({bytes_in}\d+)""",
    """\ssent=({bytes_out}\d+)""",
    """\sfw=({firewall}[a-fA-F\d.:]+)""",
    """\smsg="({alert_name}[^:"-]+?)\s*(:|"|-)""",
    """\smsg="({alert_name}Possible \w+ Flood)""",
    """\spri=({alert_severity}\d+)""",
    """\srule="({rule}[^"]+)""",
    """\sfw_action="(NA|({action}[^"]+))"""
  ]
   DupFields = [ "message_id->alert_type" 
}
```