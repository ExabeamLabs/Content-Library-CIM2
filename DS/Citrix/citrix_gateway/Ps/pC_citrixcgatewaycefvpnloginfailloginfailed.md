#### Parser Content
```Java
{
Name = citrix-cgateway-cef-vpn-login-fail-loginfailed
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "epoch"
  Conditions = [ """|Citrix|NetScaler|""", """|LOGIN_FAILED|""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}[a-fA-F:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdhost=({dest_host}[\w\-.]+)""",
    """\Wsuser=({user}[\w\.\-]{1,40}\$?)""",
    """\Wreason=({failure_reason}.+?)\s+(\w+=|$)""",
    """requestClientApplication=({user_agent}[^=]+)\s\w+="""
  ]


}
```