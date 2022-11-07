#### Parser Content
```Java
{
Name = juniper-srx-cef-network-traffic-fail-trafficdeny
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|NetScreen Traffic Deny|""" ]

cef-netscreen-network-connection = {
  Vendor = Juniper Networks
  Product = Juniper SRX
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wact=({action}.+?)(\s+[\w\-]+=|\s*$)""",
    """\Wproto=({protocol}.+?)(\s+[\w\-]+=|\s*$)""",
    """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
    """\Wspt=({src_port}\d+)""",
    """\Wshost=({src_host}.+?)(\s+[\w\-]+=|\s*$)""",
    """\Wsuser=({user}.+?)(\s+[\w\-]+=|\s*$)""",
    """\Wcat=({rule}.+?)(\s+[\w\-]+=|\s*$)""",
    """\WnitroReason=({reason}.+?)(\s+[\w\-]+=|\s*$)""",
  
}
```