#### Parser Content
```Java
{
Name = citrix-netscalar-cef-vpn-login-fail-loginfailed
  ParserVersion = v1.0.0
  Vendor = citrix
  Product = citrix netscaler
  TimeFormat = "epoch"
  Conditions = [ """|Citrix|NetScaler|""", """|LOGIN_FAILED|""" ]
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wdvc=({host}[a-fA-F:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsrc=({src_ip}[a-fA-F:\d.]+)""",
    """\Wdst=({dest_ip}[a-fA-F:\d.]+)""",
    """\Wdhost=({dest_host}[\w\-.]+)""",
    """\Wsuser=({user}\S+)""",
    """\Wreason=({failure_reason}.+?)\s+(\w+=|$)""",
    """requestClientApplication=({user_agent}[^=]+)\s\w+="""
  ]


}
```