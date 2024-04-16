#### Parser Content
```Java
{
Name = juniper-ps-kv-vpn-logout-success-closed
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""Closed connection to """
""" bytes read """
""" bytes written """
""" user="""
]
  Fields = [
    """(Juniper|PulseSecure):(\s*|(\s\S+){3}\s)({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\w{3}\s+\d{1,2}\s+\d{2}:\d{2}:\d{2}\s+({host}[\w\.-]+)\s+\S*?[\[:\s]""",
    """- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+([\w\s]+?::)?(?:({domain}\w+)\\{1,20})?(({email_address}[^@]+@[^\s]+?)|({user}[\w\.\-]{1,40}\$?))[\(\[]""",
    """\stime=\\*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\safter\s+({session_duration}\d+)\s+seconds""",
    """\swith\s+({bytes_in}\d+)\s+bytes read""",
    """\sand\s+({bytes_out}\d+)\s+bytes written"""
    """\sfw=({firewall}[a-fA-F\d.:]+)""",
    """\svpn=[\\"]*({vpn}.+?)[\\"]*(\s+\w+=|\s*$)""",
    """\srealm=[\\"]*({realm}.+?)[\\"]*(\s+\w+=|\s*$)""",
    """\sroles=[\\"]*({roles}.+?)[\\"]*(\s+\w+=|\s*$)""",
    """\sproto=({protocol}[^=]+?)(\s+\w+=|\s*$)""",
    """\ssrcport=({src_port}\d+)""",
    """\sdstip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdstname=({dest_host}[^=]+?)(\s+\w+=|\s*$)""",
    """\sport=({dest_port}\d+)""",
    """\stype=({vpn_type}[^=]+?)(\s+\w+=|\s*$)""",
    """\sop=({op}[^=]+?)(\s+\w+=|\s*$)""",
    """\sarg="({arg}[^"]+)""",
    """\sresult=({result}[^=]+?)(\s+\w+=|\s*$)""",
    """\ssent=({bytes_out}\d+)""",
    """\srcvd=({bytes_in}\d+)""",
    """\sagent="({agent}[^"]+)""",
    """\sduration=({session_duration}\d+)""",
    """\smsg=\\*"({additional_info}[^\\"]+)"""
    """exa_regex=\stime=\\*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """exa_regex=\suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)""",
    """exa_regex=\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex=\safter\s+({session_duration}\d+)\s+seconds""",
    """exa_regex=\swith\s+({bytes_in}\d+)\s+bytes read""",
    """exa_regex=\sand\s+({bytes_out}\d+)\s+bytes written"""
    """exa_regex=\sfw=({firewall}[a-fA-F\d.:]+)""",
    """exa_regex=\svpn=[\\"]*({vpn}.+?)[\\"]*(\s+\w+=|\s*$)""",
    """exa_regex=\srealm=[\\"]*({realm}.+?)[\\"]*(\s+\w+=|\s*$)""",
    """exa_regex=\sroles=[\\"]*({roles}.+?)[\\"]*(\s+\w+=|\s*$)""",
    """exa_regex=\sproto=({protocol}[^=]+?)(\s+\w+=|\s*$)""",
    """exa_regex=\ssrcport=({src_port}\d+)""",
    """exa_regex=\sdstip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_regex=\sdstname=({dest_host}[^=]+?)(\s+\w+=|\s*$)""",
    """exa_regex=\sport=({dest_port}\d+)""",
    """exa_regex=\stype=({vpn_type}[^=]+?)(\s+\w+=|\s*$)""",
    """exa_regex=\sop=({op}[^=]+?)(\s+\w+=|\s*$)""",
    """exa_regex=\sarg="({arg}[^"]+)""",
    """exa_regex=\sresult=({result}[^=]+?)(\s+\w+=|\s*$)""",
    """exa_regex=\ssent=({bytes_out}\d+)""",
    """exa_regex=\srcvd=({bytes_in}\d+)""",
    """exa_regex=\sagent="({agent}[^"]+)""",
    """exa_regex=\sduration=({session_duration}\d+)""",
    """exa_regex=\smsg=\\*"({additional_info}[^\\"]+)"""
  ]


}
```