#### Parser Content
```Java
{
Name = juniper-ps-json-vpn-logout-success-closed
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" Closed connection to """
""" bytes read """
""" bytes written """
""" user="""
""""hostname":""""
]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """\w{3}\s+\d{1,2}\s+\d{2}:\d{2}:\d{2}\s+({host}[\w\.-]+)\s+\S*?[\[:\s]""",
    """"host":.+?"name":"({host}[\w\-.]+)"""",
    """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\suser=({user}.+?)(\s+\w+=|\s*$)""",
    """\ssrc=({src_ip}[a-fA-F\d.:]+)""",
    """\safter\s+({session_duration}\d+)\s+seconds""",
    """\swith\s+({bytes_in}\d+)\s+bytes read""",
    """\sand\s+({bytes_out}\d+)\s+bytes written"""
    """\sfw=({firewall}[a-fA-F\d.:]+)""",
    """\svpn=[\\"]*({vpn}.+?)[\\"]*(\s+\w+=|\s*$)""",
    """\srealm=[\\"]*({realm}.+?)[\\"]*(\s+\w+=|\s*$)""",
    """\sroles=[\\"]*({roles}.+?)[\\"]*(\s+\w+=|\s*$)""",
    """\sproto=({protocol}[^=]+?)(\s+\w+=|\s*$)""",
    """\ssrcport=({src_port}\d+)""",
    """\sdstip=({dest_ip}[a-fA-F\d.:]+)""",
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