#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-success-connected-1
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
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
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrcport=({src_port}\d+)""",
    """\sdstip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdstname=({dest_host}[^=\|]+?)(\||\s+\w+=|\s*$)""",
    """\sport=({dest_port}\d+)""",
    """\stype=({vpn_type}[^=]+?)(\s+\w+=|\s*$)""",
    """\sop=({op}[^=]+?)(\s+\w+=|\s*$)""",
    """\sresult=({result}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wsent=({bytes_out}\d+)""",
    """\Wrcvd=({bytes_in}\d+)""",
    """\sduration=({session_duration}\d+)""",
    """\Wmsg="({additional_info}[^"]+)\s+(\d+|")"""
  ]
  DupFields = [ "user->account" ]


}
```