#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-success-passed
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd HH:mm:ss"]
    Conditions = [ 
"""Host Checker policy """
""" passed on host """
""" realm="""
]
    Fields = [
      """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\srealm="({realm}[^"]+)""",
      """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sdstip=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?""",
      """({host}[\w.\-]+) PulseSecure:""",
      """\sfw=({firewall}[a-fA-F\d.:]+)""",
      """\svpn=({vpn_client}[^=]+?)(\s+\w+=|\s*$)""",
      """\sroles="({role}[^"]+)""",
      """\sproto=({protocol}[^=]+?)(\s+\w+=|\s*$)""",
      """\ssrcport=({src_port}\d+)""",
      """\sdstname=({dest_host}[^=]+?)(\s+\w+=|\s*$)""",
      """\sport=({dest_port}\d+)""",
      """\stype=({vpn_client_type}[^=]+?)(\s+\w+=|\s*$)""",
      """\sop=({op}[^=]+?)(\s+\w+=|\s*$)""",
      """\sarg="({arg}[^"]+)""",
      """\sresult=({result}[^=]+?)(\s+\w+=|\s*$)""",
      """\ssent=({bytes_out}\d+)""",
      """\srcvd=({bytes_in}\d+)""",
      """\sagent="({agent}[^"]+)""",
      """\sduration=({session_duration}\d+)""",
      """\smsg="({additional_info}[^"]+)""",
      """\suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)"""
    ]
  

}
```