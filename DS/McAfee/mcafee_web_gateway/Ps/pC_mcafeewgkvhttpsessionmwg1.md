#### Parser Content
```Java
{
Name = mcafee-wg-kv-http-session-mwg-1
  Vendor = McAfee
  Product = McAfee Web Gateway
  TimeFormat = "yyyy-MM-dd HH:mm:ss Z"
  Conditions = [ """ mwg:""", """ host=""", """ p=""", """ dp=""" ]
  Fields = [
    """\s({host}[\w\-.]+)\smwg:\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d [+-]\d\d\d\d)\s""",
    """\shost=({host}[\w\-.]+)\s""",
    """\ss=({http_response_code}\d+)\s""",
    """\sac=({action}[^=]+)\s\w+=""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s\w+=""",
    """\sp=({protocol}[^=]+)\s\w+=""",
    """\sm=({method}[^=]+)\s\w+=""",
    """\sd=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[\w\-.]+))\s\w+=""",
    """\sdp=({dest_port}\d+)\s""",
    """\sbi=({bytes_in}\d+)\s""",
    """\sbo=({bytes_out}\d+)\s""",
    """\sup="({uri_path}[^"]+)"""",
    """\sua="({user_agent}[^"]+)"""",
    """\su=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
    """\s(breason|pfail)="({failure_reason}[^"]+)"""",
    """\s\sct="({mime}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```