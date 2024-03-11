#### Parser Content
```Java
{
Name = pan-ngfw-cef-network-traffic-trafficend
  Conditions = [ """CEF:0|Palo Alto Networks|""", """|TRAFFIC|end|""" ]
  Fields = ${PaloAltoParsersTemplates.cef-palo-alto-network-event.Fields}[
   """({event_category}TRAFFIC)""",
  ]
  ParserVersion = v1.0.0

cef-palo-alto-network-event = {
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """\sdvchost=({host}[\w.-]+?)\s+(\w+=|$)""",
    """rt=({time}\w{3}\s\d{2}\s\d{4}\s(\d{2}:){2}\d{2})\s""",
    """\ssrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s+(\w+=|$)""",
    """\sdst=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s+(\w+=|$)""",
    """\ssourceTranslatedAddress=(0.0.0.0|({src_translated_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s+(\w+=|$)""",
    """\sdestinationTranslatedAddress=(0.0.0.0|({dest_translated_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s+(\w+=|$)""",
    """\scs1=({rule}[^=]+?)\s+(\w+=|$)""",
    """\sduser=({user}[^\s@]+)@({domain}[^\s@]+)\s+(\w+=|$)""",
    """\sduser=(({domain}[^\\\s]+)?\\+)?(|({user}[^\\\s@]+))\s+(\w+=|$)""",
    """\ssuser=({user}[^\s@]+)@({domain}[^\s@]+)\s+(\w+=|$)""",
    """\ssuser=(({domain}[^\\\s]+)?\\+)?(|({user}[^\\\s@]+))\s+(\w+=|$)""", 
    """\sapp=({network_app}[^=]+?)\s+(\w+=|$)""",
    """\scs4=({src_network_zone}[^=]+?)\s+(\w+=|$)""",
    """\scs5=({dest_network_zone}[^=]+?)\s+(\w+=|$)""",
    """\sspt=(0|({src_port}\d{1,5}))\s+(\w+=|$)""",
    """\sdpt=(0|({dest_port}\d{1,5}))\s+(\w+=|$)""",
    """\ssourceTranslatedPort=(0|({src_translated_port}\d{1,5}))\s+(\w+=|$)""",
    """\sdestinationTranslatedPort=(0|({dest_translated_port}\d{1,5}))\s+(\w+=|$)""",
    """\sproto=({protocol}[^=]+?)\s+(\w+=|$)""",
    """\sact=(|({result}[^=]+?))(\s+\w+=|\s*$)""",
    """\sin=({bytes_in}\d+)\s+(\w+=|$)""",
    """\sout=({bytes_out}\d+)\s+(\w+=|$)""",
    """externalId=({alert_id}[^\s]+)""",
    """\sreason=(?:n\/a|({reason}[^=]+?))\s+(\w+=|$)""",
    """\sPanOSThreatID="*({alert_name}[^"=\(]+?)(\s*\([^\)]+?\)?)"*\s+\w+=""",
   
}
```