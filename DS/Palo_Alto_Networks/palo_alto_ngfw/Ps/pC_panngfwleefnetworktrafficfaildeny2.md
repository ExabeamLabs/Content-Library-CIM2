#### Parser Content
```Java
{
Name = pan-ngfw-leef-network-traffic-fail-deny-2
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """LEEF:""", """|deny|""", """Prisma Access""", """Palo Alto Networks""", """_globalprotect""" ]
  Fields = [
    """({action}allow)""",
    """\sSessionEndReason=({result_reason}[^\s"]+?)\s""",
    """\ssequence=({sequence}\d+)\s""",
    """\sDirection=({direction}[\w-]+)\s""",
    """\sSeverity=({severity}informational)\s""",
    """\sURLCategory=({category}[^\s]*)\s""",
    """\sMiscellaneous="(|({miscellaneous}.+?))("|\s*$)""",
    """\sdstBytes=({bytes_in}[\d.]+)\s""",
    """\ssrcBytes=({bytes_out}[\d.]+)\s""",
    """\stotalBytes=({bytes}[\d.]+)\s""",
    """\sproto=({protocol}[^\s"]+?)\s""",
    """\sdstPostNATPort=(0|({dest_translated_port}\d+))\s""",
    """\ssrcPostNATPort=(0|({src_translated_port}\d+))\s""",
    """\sdstPort=(0|({dest_port}\d+))\s""",
    """\ssrcPort=(0|({src_port}\d+))\s""",
    """\sLogForwardingProfile=({profile}[^\|]+?)\s""",
    """\sToZone=({dest_network_zone}[^\|]+?)\s""",
    """\sFromZone=({src_network_zone}[^\|]+?)\s""",
    """\sApplication=((?i)not-applicable|({network_app}[^\s]+?))\s""",
    """\sDestinationUser=(|((({dest_domain}[^\s\\]+)\\)?({dest_user}[^\s\\]+)))\\s""",
    """\sSourceUser=(|((({src_domain}[^\s\\]+)\\)?({src_user}[^\s\\]+)))\s""",
    """\susrName =(|((({domain}[^\s\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s""",
    """\sRule=({rule}[^\|]*?)\s""",
    """\sdstPostNAT=(0\.0\.0\.0|({dest_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\s""",
    """\ssrcPostNAT=(0\.0\.0\.0|({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\s""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sDeviceName =({host}[\w\-\.]+)(?=(?:\s|\||,|;)[\w.-]+=)""",
    """\sSubtype=({subtype}[^\s]*)""",
    """({action}deny)""",
    """<(?:\d{1,3})>(?:\d{0,2}\s)({time}[\w:\-\.]+)\s"""
  ]
  ParserVersion = "v1.0.0"


}
```