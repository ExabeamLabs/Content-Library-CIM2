#### Parser Content
```Java
{
Name = "catonetwork-cc-cef-vpn-logout-success-disconnect"
Vendor = "CatoNetworks"
Product = "Cato Cloud"
TimeFormat = "EEE MMM dd HH:mm:ss Z yyyy"
Conditions = [
  """CEF:"""
  """|CatoNetworks|"""
  """internalType=DISCONNECTED"""
]
Fields = [
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wrt=({time}\w+\s+\w+\s+\d+\s+\d\d:\d\d:\d\d\s+\w+\s+\d\d\d\d)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wact=({action}.+?)\s+(\w+=|$)""",
    """\Wshost=({full_name}.+?)\s+(\w+=|$)""",
    """\Wtunnel_device_type=({os}.+?)\s+(\w+=|$)""",
]
ParserVersion = "v1.0.0"


}
```