#### Parser Content
```Java
{
Name = juniper-ps-kv-vpn-login-success-connectionwith
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""PulseSecure: """
"""Established connection with type"""
"""dstname="""
]
  Fields = [
    """\s({host}[\w\-\.]+)\s*(PulseSecure|Juniper):""",
    """time="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""", 
    """\Wuser=([^\\]+\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\Wfw=({firewall}[a-fA-F\d.:]+)""",
    """\Wvpn=({vpn_client}[^=\|]+?)(\||\s+\w+=|\s*$)""",
    """\Wrealm="({realm}[^"]+)""",
    """\Wroles="({role}[^"]+)""",
    """\Wproto=({protocol}[^=\|]+?)(\||\s+\w+=|\s*$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrcport=({src_port}\d+)""",
    """\sdstip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdstname=({dest_host}[^=\|]+?)(\||\s+\w+=|\s*$)""",
    """\sport=({dest_port}\d+)""",
    """\stype=({vpn_client_type}[^=]+?)(\s+\w+=|\s*$)""",
    """\sop=({op}[^=]+?)(\s+\w+=|\s*$)""",
    """\sresult=({result}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wsent=({bytes_out}\d+)""",
    """\Wrcvd=({bytes_in}\d+)""",
    """\sduration=({session_duration}\d+)""",
    """\Wmsg="({additional_info}[^"]+)\s+(\d+|")"""
    """\Wuser=([^\\]+\\)?({account}[\w\.\-\!\#\^\~]{1,40}\$?)""",
  ]


}
```