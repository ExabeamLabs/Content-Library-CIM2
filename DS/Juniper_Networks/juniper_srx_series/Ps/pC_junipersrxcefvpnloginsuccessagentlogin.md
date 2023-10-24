#### Parser Content
```Java
{
Name = juniper-srx-cef-vpn-login-success-agentlogin
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|McAfee|ESM|""", """|Agent login succeeded|""" ]
   Fields = ${JuniperParsersTemplates.cef-juniper-vpn-events.Fields} [
    """\Wrt=({time}\d{13})""",
  ]
  ParserVersion = "v1.0.0"

cef-juniper-vpn-events = {
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "epoch"
  Fields = [
    """\s({host}[\w\-.]+)\s+CEF:""",
    """\Wrt=({time}\d+)""",
    """\WdeviceTranslatedAddress=({host}[A-Fa-f:\d.]+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wdst=({src_translated_ip}[A-Fa-f:\d.]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsuser=({user}[\w\.\-]{1,40}\$?)""",
    """\Wsuser=({email_address}[^\s@]+@[^\s@]+)""",
    """\Wact=({result}.+?)\s+(\w+=|$)""",
  ]
  DupFields = ["user->account"
}
```