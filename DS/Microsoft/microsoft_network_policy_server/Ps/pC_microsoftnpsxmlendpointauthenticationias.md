#### Parser Content
```Java
{
Name = microsoft-nps-xml-endpoint-authentication-ias
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Microsoft Network Policy Server
  TimeFormat = "MM/dd/yyyy HH:mm:ss.SSS"
  Conditions = ["""<Packet-Type data_type="0">1</Packet-Type>""", """<Client-IP-Address""", """<Authentication-Type"""]
  Fields = [
    """<Timestamp[^>]+>({time}\d+\/\d+\/\d+\s\d+:\d+:\d+\.\d+)<""",
    """<Computer-Name[^>]+>({dest_host}({host}[\w\-.]+))<""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """Fully-Qualifed-User-Name[^>]+>[^>]*?[\\\/]+?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
    """<Client-IP-Address[^>]+>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Authentication-Type[^>]+>({auth_method}[^<]+)<""",
    """Proxy-Policy-Name[^>]+>({additional_info}[^<]+)<""",
    """<Packet-Type.+?>({result}\d+)""",
    """<NP-Policy-Name[^>]+>({network}[^<]+)""",
    """<SAM-Account-Name[^>]+>(({domain}[^<\\]+)\\)?({account}[^<]+)""",
    """<NAS-IP-Address data_type=[^>]+>({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})<""",
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "result->event_code" ]


}
```