#### Parser Content
```Java
{
Name = ivanti-ps-kv-network-close-success-nwc32001
  Conditions = [ """ PulseSecure: """, """NWC32001""", """ type=vpnssl """, """Client connection done""" ]
  Fields = ${JuniperParsersTemplates.ivanti-pulsesecure-events.Fields}[
    """({event_name}Client connection done)"""
  ]
  ParserVersion = "v1.0.0"

ivanti-pulsesecure-events = {
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\s({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+)))\sPulseSecure:""",
    """\stime="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """\ssrc=({src_ip}[A-Fa-f\d:.]+)\s""",
    """\suser=(system|anonymous|({user}[\w\.\-]{1,40}\$?)(@({domain}[^=]+?))?)\s\w+=""",
    """\srealm="({realm}[^"]+)"""",
    """\smsg="({additional_info}.+?)$""",
    """\sfw=({firewall}[^\s]+)\s\w+""",
    """\sroles="({role}[^"]+)"""",
    """\svpn=({vpn}[^=]+)\s\w+=""",
    """\sproto=({protocol}[^=]+)\s\w+=""",
    """\stype=({vpn_type}[^=]+)\s\w+=""",
    """\smsg="({event_code}\w+):""",
    """\smsg_code=({event_code}\w+)\s\w+=""",
    """\sagent="({user_agent}[^"]+)"""",
    """\ssession_id=({session_id}[^\s]+)"""
  
}
```