#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-success-passed
    ParserVersion = v1.0.0
    Vendor = Juniper Networks
    Product = Juniper Pulse Secure
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ 
"""Host Checker policy """
""" passed on host """
""" realm=""" 
]
    Fields = [
      """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\suser=({user}[^\s].*?)(\s+\w+=|\s*$)""",
      """\srealm="({realm}[^"]+)""",
      """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sdstip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """({host}[\w.\-]+) PulseSecure:""",
      """\sfw=({firewall}[a-fA-F\d.:]+)""",
      """\svpn=({vpn}[^=]+?)(\s+\w+=|\s*$)""",
      """\sroles="({roles}[^"]+)""",
      """\sproto=({protocol}[^=]+?)(\s+\w+=|\s*$)""",
      """\ssrcport=({src_port}\d+)""",
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
      """\smsg="({additional_info}[^"]+)""",
    ]
    DupFields = [ "dest_ip->host" , "user->account" ]
  

}
```