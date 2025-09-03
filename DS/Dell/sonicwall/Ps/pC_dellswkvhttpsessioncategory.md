#### Parser Content
```Java
{
Name = dell-sw-kv-http-session-category
  ParserVersion = v1.0.0
  Conditions = [
    """ m=97 """,
    """id=""",
    """ fw=""",
    """ c=1024 """,
    """ pri=""",
    """ src=""",
    """ dst="""
  ]
  Fields = ${SonicwallParsersTemplates.sonicwall-firewall.Fields} [
    """Category="({category}[^"]+)""",
    """dstname=(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}[^"\/\s]+))"""
  ]

sonicwall-firewall = {
  Vendor = Dell
  Product = Sonicwall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """time=(\\)?"({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d)"""
    """usr="\s*(({email_address}[^@"]+@[^\\\s"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\smsg="({additional_info}[^"]+?)\s*"""",
    """\sc=({category_id}\d+)""",
    """\sm=({message_id}\d+)""",
    """\sipscat="({category}[^"]+)""",
    """\sipspri=({alert_severity}\d+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(:({src_interface}[^\s:]+))?(:[^\s:]+)?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(:({dest_interface}[^\s:]+))?(:[^\s:]+)?""",
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