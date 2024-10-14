#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-logout-success-sessiontimedout
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd HH:mm:ss"]
  Conditions = [ """ PulseSecure: """, """session timeout for""", """ (session:""" ]
  Fields = [
    """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s\d"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({host}[\w\-.]+)\sPulseSecure:""",
    """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+([\w\s]+?::)?(({email_address}[^@\s]+@[^.\s]+\.[^\s]+)|({full_name}[^,\[]+,[^\[]+)|(({domain}[^\\\(]+)\\)?(System|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\(({realm}[^\)]+)?\)\[({resource}[^\]]+)?\]""",
    """session timeout for (({email_address}[^@\s\/]+@[^.\s\/]+\.[^\s\/]+)|({full_name}[^,\/]+,[^\/]+)|(({domain}[^\\\/]+)\\)?|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\/""",
    """\s\(({additional_info}session:[^\)]+)\)"""
    """\suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\/]+)[\/\\]+)?({user}[\w\.\-]{1,40}))(\s+\w+=|\s*$)"""
    """\stime="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """\ssrc=({src_ip}[A-Fa-f\d:.]+)\s""",
    """\suser=(({user}[\w\.\-]{1,40}\$?)(@({domain}[^=]+?))?)\s\w+=""",
    """\suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)[\/\\]+)?({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)"""
    """\srealm="({realm}[^"]+)"""",
    """\smsg="({additional_info}.+?)$""",
    """\sfw=({firewall}[^\s]+)\s\w+""",
    """\sroles="({role}[^"]+)"""",
    """\svpn=({vpn_client}[^=]+)\s\w+=""",
    """\sproto=({protocol}[^=]+)\s\w+=""",
    """\stype=({vpn_client_type}[^=]+)\s\w+=""",
    """\smsg="({event_code}\w+):""",
    """\smsg_code=({event_code}\w+)\s\w+=""",
  ]
  ParserVersion = "v1.0.0"


}
```