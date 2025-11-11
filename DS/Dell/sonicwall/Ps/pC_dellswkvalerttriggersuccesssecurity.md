#### Parser Content
```Java
{
Name = dell-sw-kv-alert-trigger-success-security
  ParserVersion = "v1.0.0"
  Product = Sonicwall
  Conditions = [ """ m=""", """id=""", """ fw=""", """ c=""" ,""" msg="""", """ pri=1 """, """ src=""", """ dst="""]
  Fields = ${SonicwallDLParsersTemplates.sonicwall-firewall-dl.Fields} [
  """\smsg="({alert_subject}[^:"-]+?)\s*(:|"|-)"""
  ]

sonicwall-firewall-dl = {
  Vendor = Dell
  Product = Sonicwall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
     """time=(\\)?"({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d)"""
    """\smsg="({event_name}[^:"]+?)\s*(:|")""",
    """\snote="\s*({additional_info}[^"]+?)\s*"""",
    """\sc=({category_id}\d+)""",
    """\sm=({alert_type}({message_id}\d+))""",
    """\suser="\s*(({email_address}[^@"]+@[^\\\s"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """usr="\s*(({email_address}[^@"]+@[^\\\s"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({src_port}\d+))?(:({src_interface}[^\s:]+))?(:[^\s:]+)?""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({dest_port}\d+))?(:({dest_interface}[^\s:]+))?(:[^\s:]+)?""",
    """\ssrcMac=({src_mac}[a-fA-F\d.:]+)""",
    """\sdstMac=({dest_mac}[a-fA-F\d.:]+)""",
    """\sproto=({protocol}[^\s\/\d"]+)""",
    """\sfw=({firewall}[a-fA-F\d.:]+)""",
    """\spri=({severity}\d+)""",
    """\sfw_action="(NA|({action}[^\s"]+))""",
    """\sfw_action="(NA|({action}[^\s"]+))""",
    """\smsg="({alert_name}[^:"-]+?)\s*(:|"|-)""",
    """\smsg="({alert_name}Possible \w+ Flood)""",
    """\spri=({alert_severity}\d+)""",
    """\smsg="({additional_info}[^"]+?)\s*"""",
    """\srule="({rule}[^"]+)"""
    """rpkt=({packets_in}\d+)"""
    """spkt=({packets_out}\d+)"""
  
}
```