#### Parser Content
```Java
{
Name = juniper-srx-cef-network-traffic-success-sessionclosed
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|RT_FLOW_SESSION_CLOSE|""", """|Session closed|""" ]
  Fields = [
    """\sproto=({protocol}\w+)""",
    """\sin=({bytes_in}\d+)""",
    """\sout=({bytes_out}\d+)""",
    """\srt=({time}\d{13})""",
    """\sshost=(|({src_host}.+?))(\s+\w+=|\s*$)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\ssourceTranslatedAddress=({src_translated_ip}[a-fA-f\d.:]+)""",
    """\sspt=({src_port}\d+)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdestinationTranslatedAddress=({dest_translated_ip}[a-fA-F\d.:]+)""",
    """\sdpt=({dest_port}\d+)""",
    """\sduser=(|N\/A|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)""",
    """\sdvc=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\sdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\sreason=(|({failure_reason}.+?))(\s+\w+=|\s*$)""",
    """\sdeviceInboundInterface=(|({dest_interface}.+?))(\s+\w+=|\s*$)""",
  ]


}
```