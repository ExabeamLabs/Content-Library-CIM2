#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-success-sessionresumed
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Juniper|""", """|Session resumed|""" ]
  Fields = [
        """\Wrt=({time}\d+)""",
        """\Wdvchost=({host}[\w\-.]+)""",
        """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
        """\Wsuser=(System|({user}[^\s]+))""",
        """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsproc=({realm}.+?)\s+\w+=""",
    """\Wspriv=({resource}.+?)\s+\w+=""",
    """({event_code}Session resumed)""",
    """dst=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
  ]
  DupFields = [ "host->dest_host" , "user->account"]
  ParserVersion = "v1.0.0"


}
```