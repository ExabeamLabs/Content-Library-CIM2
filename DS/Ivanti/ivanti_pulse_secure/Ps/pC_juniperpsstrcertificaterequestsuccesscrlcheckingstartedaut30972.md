#### Parser Content
```Java
{
Name = juniper-ps-str-certificate-request-success-crlcheckingstarted-aut30972
  Conditions = [ """ PulseSecure: """, """AUT30972""", """CRL checking started for certificate"""]
  Fields = ${JuniperParsersTemplates.ivanti-pulsesecure-events.Fields}[
    """msg="({event_code}\w+):\s+({additional_info}[^\$]+?)\s*$""",
  ]
  ParserVersion = "v1.0.0"

ivanti-pulsesecure-events = {
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\s({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+)))\sPulseSecure:""",
    """\stime="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """\ssrc=({src_ip}[A-Fa-f\d:.]+)\s""",
    """\suser=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^=]+?))?)\s\w+=""",
    """\suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\/]+)[\/\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
    """\srealm="({realm}[^"]+)"""",
    """\smsg="({additional_info}.+?)$""",
    """\sfw=({firewall}[^\s]+)\s\w+""",
    """\sroles="(|({role}[^=]+?))"\s\w+=""",
    """\svpn=({vpn_client}[^=]+)\s\w+=""",
    """\sproto=({protocol}[^=]+)\s\w+=""",
    """\stype=({vpn_client_type}[^=]+)\s\w+=""",
    """\smsg="({event_code}\w+):""",
    """\smsg_code=({event_code}\w+)\s\w+=""",
    """\sagent="(|({user_agent}[^"]+?))"\s\w+=""",
    """\ssession_id=({session_id}[^\s]+)"""
  
}
```