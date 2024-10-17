#### Parser Content
```Java
{
Name = "pan-gp-sk4-vpn-login-gatewayprelogin"
 ParserVersion = "v1.0.0"
 Conditions = [ """PanOSEventIDValue=gateway-prelogin""", """GLOBALPROTECT""" ]

paloalto-vpn-event = {
   Vendor = Palo Alto Networks
   Product = GlobalProtect
   TimeFormat = "epoch"
   Fields = [
       """\srt=({time}\d{13})""",
       """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
       """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
       """\ssuser=(({domain}[^\\=]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
       """\sdvchost=({host}[\w\-.]+?)\s+\w+=""",
       """\scs2=({result}[^=]+)\s+\w+=""",
       """\smsg=({event_name}[^=]+?)\s+\w+=""",
       """cs6=({os}[^=]+?)\s+\w+=""",
       """sourceGeoCountryCode=({src_country}[^=]+?)\s+\w+=""",
       """({app}GLOBALPROTECT)"""
     ]
 },

cef-palo-alto-networks-firewall = {
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = ["epoch", "MMM dd yyyy HH:mm:ss z", "MMM dd yyyy HH:mm:ss", "yyyy/MM/dd HH:mm:ss","epoch_sec"]
  Fields = [
    """\sdvchost=({host}.+?)\s+(\w+=|$)""",
    """\Wrt=({time}\d+\/\d+\/+\d+\s+\d+:\d+:\d+)"""
    """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+)\s+\w+""",
    """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+\w+)\s+\w+(:|=)""",
    """\srt=({time}\d{10})\s+(\w+=|$)"""
    """\srt=({time}\d{13})\s+(\w+=|$)""",
    """\sduser=(?=[^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s@]+)\s+(\w+=|$)""",
    """\sduser=(?!\S+@\S+)(({domain}[^\\\s]+)?\\+)?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)""",
    """\ssuser=(?=[^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s@]+)\s+(\w+=|$)""",
    """\ssuser=(?!\S+@\S+)(({domain}[^\\\s]+)?\\+)?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)""",
    """({event_category}TRAFFIC)""",
    """\|({subtype}[^\|]+)\|TRAFFIC""",
    """\scs1=({rule}.+?)\s+(\w+=|$)""",
    """\sshost=({src_host}.+?)\s+(\w+=|$)""",
    """\sdhost=({dest_host}.+?)\s+(\w+=|$)""",
    """\ssrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+(\w+=|$)""",
    """\sdst=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+(\w+=|$)""",
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
    """\sreason=(?:n\/a|({result_reason}.+?))\s+(\w+=|$)""",
  ]
  DupFields = [ "subtype->action" 
}
```