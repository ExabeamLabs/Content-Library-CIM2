#### Parser Content
```Java
{
Name = dell-sw-kv-app-activity-appactivity
  Conditions = [
    """ m=""",
    """id=""",
    """ fw=""",
    """ c=""",
    """ pri="""
  ]
  ParserVersion = "v1.0.0"

sonicwall-firewall = {
  Vendor = Dell
  Product = Sonicwall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """time="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """\smsg="({event_name}[^:"]+?)\s*(:|")""",
    """\snote="\s*({additional_info}[^"]+?)\s*"""",
    """\sc=({category_id}\d+)""",
    """\sm=({message_id}\d+)""",
    """\suser="\s*(({email_address}[^@"]+@[^\\\s"]+)|({user}[^\\\s"]+))""",
    """usr="\s*(({email_address}[^@"]+@[^\\\s"]+)|({user}[^\\\s"]+))""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({src_port}\d+))?(:({src_interface}[^\s:]+))?(:[^\s:]+)?""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({dest_port}\d+))?(:({dest_interface}[^\s:]+))?(:[^\s:]+)?""",
    """\ssrcMac=({src_mac}[a-fA-F\d.:]+)""",
    """\sdstMac=({dest_mac}[a-fA-F\d.:]+)""",
    """\sproto=({protocol}[^\s\/\d"]+)""",
    """\sfw=({firewall}[a-fA-F\d.:]+)""",
    """\spri=({severity}\d+)""",
    """\sfw_action="(NA|({action}[^\s"]+))"""
  
}
```