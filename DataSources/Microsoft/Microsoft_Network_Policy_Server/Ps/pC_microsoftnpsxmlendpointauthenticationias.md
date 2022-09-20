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
    """<Computer-Name[^>]+>({host}[^<]+)<""",
    """Fully-Qualifed-User-Name[^>]+>[^>]*?[\\\/]+?({user}[^\\\/]*?)<""",
    """<Client-IP-Address[^>]+>({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """<Authentication-Type[^>]+>({auth_method}[^<]+)<""",
    """Proxy-Policy-Name[^>]+>({additional_info}[^<]+)<""",
    """<Packet-Type.+?>({result}\d+)""",
    """<NP-Policy-Name[^>]+>({network}[^<]+)""",
    """<SAM-Account-Name[^>]+>(({domain}[^<\\]+)\\)?({account}[^<]+)""",
    """<NAS-IP-Address data_type=[^>]+>({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})<""",
  ]
  DupFields = [ "host->dest_host","result->event_code" ]


}
```