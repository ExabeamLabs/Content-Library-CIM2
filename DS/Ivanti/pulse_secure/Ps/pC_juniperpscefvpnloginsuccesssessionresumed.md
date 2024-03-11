#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-success-sessionresumed
  Vendor = Ivanti
  Product = Pulse Secure
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Juniper|""", """|Session resumed|""" ]
  Fields = [
        """\Wrt=({time}\d{13})""",
        """\Wdvchost=({host}[\w\-.]+)""",
        """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """\Wsuser=(System|({user}[^\s]+))""",
        """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsproc=({realm}.+?)\s+\w+=""",
    """\Wspriv=({resource}.+?)\s+\w+=""",
    """({event_code}Session resumed)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]
  DupFields = [ "host->dest_host" , "user->account"]
  ParserVersion = "v1.0.0"


}
```