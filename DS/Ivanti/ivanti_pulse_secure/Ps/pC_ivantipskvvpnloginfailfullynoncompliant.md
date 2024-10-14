#### Parser Content
```Java
{
Name = ivanti-ps-kv-vpn-login-fail-fullynoncompliant
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """Host Checker Compliance Result""", """['Fully Non Compliant']""", """PulseSecure:""" ]
    Fields = ${JuniperParsersTemplates.ivanti-pulsesecure-events.Fields}[
      """({result}Fully Non Compliant)""",
      """failed_reasons: \['({failure_reason}.+?)'\]""",
      """ for user \['(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'\]""",
      """ on host \['({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'\]"""
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)\s+PulseSecure:"""
    ]
 
ivanti-pulsesecure-events = {
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\s({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+)))\sPulseSecure:""",
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