#### Parser Content
```Java
{
Name = fortinet-fortigate-kv-network-traffic-fail-traffic
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Fortinet|FortiGate-""", """traffic deny|""" ]
 
fortinet-fortigate-cef-network-traffic-info {
 Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [ 
    """\Wstart=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """\Wtz="?({tz}[+-]\d+)"?"""
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\Wproto=({protocol}\w+)""",
    """\Wsubtype=({category}\w+)""",
    """\Wact=(|({action}.+?))(\s+\w+=|\s*$)""",
    """\Wshost=(|({src_host}.+?))(\s+\w+=|\s*$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wspt=({src_port}\d+)""",
    """\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdpt=({dest_port}\d+)""",
    """\WdeviceOutboundInterface=({dest_interface}.+?)(\s+\w+=|\s*$)""",
    """\WdeviceInboundInterface=({src_interface}.+?)(\s+\w+=|\s*$)""",
    """\Wout=({bytes_out}\d+)""",
    """\Win=({bytes_in}\d+)""",
    """xauthuser=(N\/A|({user}\w+))""",
    """\Wsrccountry=((?i)reserved|({src_country}\w+))""",
    """\Wdstcountry=((?i)reserved|({dest_country}\w+))"""
  
}
```