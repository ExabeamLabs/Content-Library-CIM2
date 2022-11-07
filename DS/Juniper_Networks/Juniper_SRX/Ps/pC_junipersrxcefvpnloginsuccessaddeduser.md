#### Parser Content
```Java
{
Name = juniper-srx-cef-vpn-login-success-addeduser
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|McAfee|ESM|""", """|SecureAccess_v7 Added user to authentication server|""" ]

cef-juniper-vpn-events = {
  Vendor = Juniper Networks
  Product = Juniper SRX
  TimeFormat = "epoch"
  Fields = [
    """\s({host}[\w\-.]+)\s+CEF:""",
    """\Wrt=({time}\d+)""",
    """\WdeviceTranslatedAddress=({host}[A-Fa-f:\d.]+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wdst=({src_translated_ip}[A-Fa-f:\d.]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsuser=({user}[^\s"@]+)""",
    """\Wsuser=({email_address}[^\s@]+@[^\s@]+)""",
    """\Wact=({action}.+?)\s+(\w+=|$)""",
  ]
  DupFields = ["user->account"
}
```