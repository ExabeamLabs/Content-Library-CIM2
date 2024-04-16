#### Parser Content
```Java
{
Name = pan-ngfw-cef-network-traffic-success-end
  ParserVersion = v1.0.0
  Conditions = [
"""Palo Alto Networks|PAN-OS|""",
"""|end|TRAFFIC|"""
  ]

cef-palo-alto-networks-firewall = {
    Vendor = Palo Alto Networks
    TimeFormat = "epoch"
    Fields = [
      """\sdvchost=({host}.+?)\s+(\w+=|$)""",
      """\srt=({time}\d{13})\s+(\w+=|$)""",
      """\sduser=(?=[^\s]+@[^\s]+)({user}[\w\.\-]{1,40}\$?)@({domain}[^\s@]+)\s+(\w+=|$)""",
      """\sduser=(?!\S+@\S+)(({domain}[^\\]+)?\\+)?(|({user}[\w\.\-]{1,40}\$?))\s+(\w+=|$)""",
      """\ssuser=(?=[^\s]+@[^\s]+)({user}[\w\.\-]{1,40}\$?)@({domain}[^\s@]+)\s+(\w+=|$)""",
      """\ssuser=(?!\S+@\S+)(({domain}[^\\]+)?\\+)?(|({user}[\w\.\-]{1,40}\$?))\s+(\w+=|$)""",
      """({event_category}TRAFFIC)""",
      """\|({subtype}[^\|]+)\|TRAFFIC""",
      """\scs1=({rule}.+?)\s+(\w+=|$)""",
      """\sshost=({src_host}.+?)\s+(\w+=|$)""",
      """\sdhost=({dest_host}.+?)\s+(\w+=|$)""",
      """\ssrc=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s+(\w+=|$)""",
      """\sdst=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s+(\w+=|$)""",
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
      """\sin=({bytes_in}\d+)\s+(\w+=|$)""",
      """\sout=({bytes_out}\d+)\s+(\w+=|$)""",
      """\scs2=({category}.+?)\s+(\w+=|$)""",
      """\sseverity=({severity}.+?)\s+(\w+=|$)""",
      """\sdeviceDirection=({direction}.+?)\s+(\w+=|$)""",
      """\scategoryOutcome=\/?({result}.+?)\s+(\w+=|$)""",
      """\sreason=(?:n\/a|({result_reason}.+?))\s+(\w+=|$)""",
    ]
    DupFields = [ "subtype->action" 
}
```