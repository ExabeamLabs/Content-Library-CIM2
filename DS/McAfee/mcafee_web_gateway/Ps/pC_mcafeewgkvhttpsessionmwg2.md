#### Parser Content
```Java
{
Name = mcafee-wg-kv-http-session-mwg-2
  Vendor = McAfee
  Product = McAfee Web Gateway
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """ mwg:""", """ status="""", """ proto="""", """ mt="""" ]
  Fields = [
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-.]+)\smwg:""",
    """\sstatus="({http_response_code}\d+)""",
    """\ssrcip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\sdestip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """\sproto="({protocol}\w+)""",
    """\smt="({mime}[^"]+)"""",
    """\suser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  ]
  ParserVersion = "v1.0.0"


}
```