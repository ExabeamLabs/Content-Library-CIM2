#### Parser Content
```Java
{
Name = ivanti-ps-kv-vpn-logout-success-aut22927
    Conditions = ["""PulseSecure:""", """AUT22927:""", """type=vpn""", """proto=auth""" ]
    ParserVersion = v1.0.0

ivanti-pulsesecure-events = {
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\s({host}[\w\-.]+)\sPulseSecure:""",
    """\stime="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """\ssrc=({src_ip}[A-Fa-f\d:.]+)\s""",
    """\suser=({user}[^=@]+?)(@({domain}[^=]+?))?\s\w+=""",
    """\srealm="({realm}[^"]+)"""",
    """\smsg="({additional_info}.+?)$""",
    """\sfw=({firewall}[^\s]+)\s\w+""",
    """\sroles="({role}[^"]+)"""",
    """\svpn=({vpn}[^=]+)\s\w+=""",
    """\sproto=({protocal}[^=]+)\s\w+=""",
    """\stype=({vpn_type}[^=]+)\s\w+=""",
    """\smsg="({event_code}\w+):"""
  ]
  DupFields = [ "host->dest_host" 
}
```