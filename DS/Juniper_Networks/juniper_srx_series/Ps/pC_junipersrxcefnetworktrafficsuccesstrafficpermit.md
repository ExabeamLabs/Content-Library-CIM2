#### Parser Content
```Java
{
Name = juniper-srx-cef-network-traffic-success-trafficpermit
  TimeFormat = "epoch"
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|NetScreen Traffic Permit|""" ]
  Fields = ${JuniperParsersTemplates.cef-netscreen-network-connection.Fields} [
    """\Wrt=({time}\d{13})""",
  ]

cef-netscreen-network-connection = {
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wact=({action}.+?)(\s+[\w\-]+=|\s*$)""",
    """\Wproto=({protocol}.+?)(\s+[\w\-]+=|\s*$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wspt=({src_port}\d+)""",
    """\Wshost=({src_host}.+?)(\s+[\w\-]+=|\s*$)""",
    """\Wsuser=({user}.+?)(\s+[\w\-]+=|\s*$)""",
    """\Wcat=({rule}.+?)(\s+[\w\-]+=|\s*$)""",
    """\WnitroReason=({reason}.+?)(\s+[\w\-]+=|\s*$)""",
  
}
```