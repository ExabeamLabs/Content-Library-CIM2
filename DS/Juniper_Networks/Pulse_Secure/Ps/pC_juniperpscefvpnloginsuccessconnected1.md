#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-success-connected-1
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""PulseSecure: """
""" Connected to """
"""dstname="""
]
  Fields = [
    """\s({host}[\w\-\.]+)\s*(PulseSecure|Juniper):""",
    """time="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""", 
    """\Wuser=([^\\]+\\)?({user}[^\s\|]+)""",
    """\Wfw=({firewall}[a-fA-F\d.:]+)""",
    """\Wvpn=({vpn}[^=\|]+?)(\||\s+\w+=|\s*$)""",
    """\Wrealm="({realm}[^"]+)""",
    """\Wroles="({roles}[^"]+)""",
    """\Wproto=({protocol}[^=\|]+?)(\||\s+\w+=|\s*$)""",
    """\Wsrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\Wdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\ssrcport=({src_port}\d+)""",
    """\sdstip=({dest_ip}[a-fA-F\d.:]+)""",
    """\Wdstname=({dest_host}[^=\|]+?)(\||\s+\w+=|\s*$)""",
    """\sport=({dest_port}\d+)""",
    """\stype=({vpn_type}[^=]+?)(\s+\w+=|\s*$)""",
    """\sop=({op}[^=]+?)(\s+\w+=|\s*$)""",
    """\sresult=({result}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wsent=({bytes_out}\d+)""",
    """\Wrcvd=({bytes_in}\d+)""",
    """\sduration=({session_duration}\d+)"""
  ]
  DupFields = [ "user->account" ]


}
```