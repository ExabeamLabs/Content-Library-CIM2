#### Parser Content
```Java
{
Name = pan-ngfw-cef-network-traffic-fail-drop
  ParserVersion = v1.0.0
  Conditions = [
"""Palo Alto Networks|PAN-OS|""",
"""|drop|TRAFFIC|"""
  ]
  Fields = ${PaloAltoParsersTemplates.cef-palo-alto-networks-firewall.Fields}[
     """\sreason=(?:n\/a|({failure_reason}.+?))\s+(\w+=|$)"""
 ]

cef-palo-alto-networks-firewall = {
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "epoch"
  Fields = [
    """\sdvchost=({host}.+?)\s+(\w+=|$)""",
    """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+\w+)""",
    """\srt=({time}\d{13})\s+(\w+=|$)""",
    """\sduser=(?=[^\s]+@[^\s]+)({user}[^\s@]+)@({domain}[^\s@]+)\s+(\w+=|$)""",
    """\sduser=(?!\S+@\S+)(({domain}[^\\\s]+)?\\+)?(|({user}[^\\\s]+))\s+(\w+=|$)""",
    """\ssuser=(?=[^\s]+@[^\s]+)({user}[^\s@]+)@({domain}[^\s@]+)\s+(\w+=|$)""",
    """\ssuser=(?!\S+@\S+)(({domain}[^\\\s]+)?\\+)?(|({user}[^\\\s]+))\s+(\w+=|$)""",
    """({event_category}TRAFFIC)""",
    """\|({subtype}[^\|]+)\|TRAFFIC""",
    """\scs1=({rule}.+?)\s+(\w+=|$)""",
    """\sshost=({src_host}.+?)\s+(\w+=|$)""",
    """\sdhost=({dest_host}.+?)\s+(\w+=|$)""",
    """\ssrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+(\w+=|$)""",
    """\sdst=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+(\w+=|$)""",
    """\ssourceTranslatedAddress=(0.0.0.0|({src_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}))\s+(\w+=|$)""",
    """\sdestinationTranslatedAddress=(0.0.0.0|({dest_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}))\s+(\w+=|$)""",
    """\sspt=(0|({src_port}\d+))\s+(\w+=|$)""",
    """\sdpt=(0|({dest_port}\d+))\s+(\w+=|$)""",
    """\ssourceTranslatedPort=(0|({src_translated_port}\d+))\s+(\w+=|$)""",
    """\sdestinationTranslatedPort=(0|({dest_translated_port}\d+))\s+(\w+=|$)""",
    """\sapp=({network_app}.+?)\s+(\w+=|$)""",
    """\scs4=({src_network_zone}.+?)\s+(\w+=|$)""",
    """\scs5=({dest_network_zone}.+?)\s+(\w+=|$)""",
    """\scs6=({profile}.+?)\s+(\w+=|$)""",
    """\sproto=({protocol}.+?)\s+(\w+=|$)""",
    """\sin=({bytes_in}[\d.]+)\s+(\w+=|$)""",
    """\sout=({bytes_out}[\d.]+)\s+(\w+=|$)""",
    """\scs2=({category}.+?)\s+(\w+=|$)""",
    """\sseverity=({severity}.+?)\s+(\w+=|$)""",
    """\sdeviceDirection=({direction}.+?)\s+(\w+=|$)""",
    """\scategoryOutcome=\/?({result}.+?)\s+(\w+=|$)""",
    """\sreason=(?:n\/a|({reason}.+?))\s+(\w+=|$)""",
  ]
  DupFields = [ "subtype->action" 
}
```