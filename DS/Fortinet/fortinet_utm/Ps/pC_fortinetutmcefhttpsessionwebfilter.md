#### Parser Content
```Java
{
Name = fortinet-utm-cef-http-session-webfilter
  Vendor = Fortinet
  Product = Fortinet UTM
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Fortinet|FortiGate-VM|""", """|webfilter""" ]
  Fields = [
    """\Wrt=({time}\d{13})\s+(\w+=|$)""",
    """\Wdvc=({host}.+?)\s+(\w+=|$)""",
    """\Wdvchost=({host}.+?)\s+(\w+=|$)""",
    """\Wact=({action}.+?)\s+(\w+=|$)""",
    """\Wcat=({categories}({category}[^;,=]+)[^=]*?)\s+(\w+=|$)""",
    """\Wduser=({user}[^\s@]+)\s+(\w+=|$)""",
    """\Wduser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(\w+=|$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+(\w+=|$)""",
    """\Wshost=({src_host}.+?)\s+(\w+=|$)""",
    """\Wdhost=({dest_host}.+?)\s+(\w+=|$)""",
    """\Wapp=({protocol}.+?)\s+(\w+=|$)""",
    """\Wmsg=({additional_info}.+?)\s+(\w+=|$)""",
    """\Win=({bytes_in}\d*)\s+(\w+=|$)""",
    """\Wout=({bytes_out}\d*)\s+(\w+=|$)""",
    """\Wrequest=(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({web_domain}[^\\\/\s:,"]+))?(:({dest_port}\d+))?({uri_path}\/[^\?",]*?)?({uri_query}\?[^"]*?)?))\s+(\w+=|$)""",
    """\Wspt=({src_port}\d*)\s+(\w+=|$)""",
    """\Wdpt=({dest_port}\d*)\s+(\w+=|$)""",
    """\Wdhost=({web_domain}.+?)\s+(\w+=|$)""",
  ]
  ParserVersion = "v1.0.0"


}
```