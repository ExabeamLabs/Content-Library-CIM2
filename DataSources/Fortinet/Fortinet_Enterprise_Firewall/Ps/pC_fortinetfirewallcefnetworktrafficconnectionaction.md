#### Parser Content
```Java
{
Name = fortinet-firewall-cef-network-traffic-connectionaction
  Vendor = Fortinet
  Product = Fortinet Enterprise Firewall
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ 
"""CEF:"""
"""|Fortinet|Fortigate|"""
"""cn1Label=Duration"""
"""|traffic: """
]
  Fields = [
    """\Wproto=({protocol}\w+)""",
    """\Wact=(|({action}.+?))(\s+\w+=|\s*$)""",
    """\Wrt=({time}\d+)""",
    """\Wshost=(|({src_host}.+?))(\s+\w+=|\s*$)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
    """\Wspt=({src_port}\d+)""",
    """\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\WdestinationServiceName =(|({service_name}.+?))(\s+\w+=|\s*$)""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\WdeviceOutboundInterface=({dest_interface}.+?)(\s+\w+=|\s*$)""",
    """\WdeviceInboundInterface=({src_interface}.+?)(\s+\w+=|\s*$)""",
    """\Wout=({bytes_out}\d+)""",
    """\Win=({bytes_in}\d+)"""
]


}
```