#### Parser Content
```Java
{
Name = juniper-ps-kv-vpn-logout-success-closed
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""" Closed connection to """
""" bytes read """
""" bytes written """
""" user="""
]
  Fields = [
    """(Juniper|PulseSecure):(\s*|(\s\S+){3}\s)({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\w{3}\s+\d{1,2}\s+\d{2}:\d{2}:\d{2}\s+({host}[\w\.-]+)\s+\S*?[\[:\s]""",
    """- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+([\w\s]+?::)?(?:({domain}\w+)\\{1,20})?(({email_address}[^@]+@[^\s]+?)|({user}[^\(\[]+?))[\(\[]""",
    """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\suser=(({email_address}[^@\s]+@[^\.\s]+\.[^\s]+)|({user}[^\s]+?))(\s+\w+=|\s*$)""",
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
    """\smsg="({additional_info}[^"]+)"""
  ]


}
```