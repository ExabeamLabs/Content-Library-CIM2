#### Parser Content
```Java
{
Name = "juniper-ps-kv-vpn-login-success-23464"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" id="""
"""NWC23464"""
"""Session started"""
]
Fields = [
"""({host}[\w\-\.]+)\s*(PulseSecure|Juniper):"""
"""\stime="+({time}\d+-\d+-\d+ \d+:\d+:\d+).+?user"""
"""\suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
"""with IP(v4 address)?\s+({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sfw=({firewall}[a-fA-F\d.:]+)"""
"""\svpn=({vpn_client}[^=]+?)(\s+\w+=|\s*$)"""
"""\srealm="({realm}[^"]+)"""
"""\sroles="({role}[^"]+)"""
"""\sproto=({protocol}[^=]+?)(\s+\w+=|\s*$)"""
"""\ssrcport=({src_port}\d+)"""
"""\sdstip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdstname=({dest_host}[^=]+?)(\s+\w+=|\s*$)"""
"""\sport=({dest_port}\d+)"""
"""\stype=({vpn_client_type}[^=]+?)(\s+\w+=|\s*$)"""
"""\sop=({op}[^=]+?)(\s+\w+=|\s*$)"""
"""\sarg="({arg}[^"]+)"""
"""\sresult=({result}[^=]+?)(\s+\w+=|\s*$)"""
"""\ssent=({bytes_out}\d+)"""
"""\srcvd=({bytes_in}\d+)"""
"""\sagent="({agent}[^"]+)"""
"""\sduration=({session_duration}\d+)"""
"""\smsg="({additional_info}[^"]+)"""
"""hostname\s+({src_host}[^"]+)"""
]
DupFields = [
"user->account"
]
ParserVersion = "v1.0.0"


}
```