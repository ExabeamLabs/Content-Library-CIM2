#### Parser Content
```Java
{
Name = microsoft-nps-xml-endpoint-authentication-packettype4
  Vendor = Microsoft
  Product = Microsoft Network Policy Server
  TimeFormat = "MM/dd/yyyy HH:mm:ss.SSS"
  Conditions = ["""<Packet-Type data_type="0">4</Packet-Type>""", """<Client-IP-Address""", """<Computer-Name"""]
  Fields = [
    """<Timestamp[^>]+>({time}\d+\/\d+\/\d+\s\d+:\d+:\d+\.\d+)<""",
    """<Computer-Name[^>]+>({host}[^<]+)<""",
    """<User-Name[^>]+>(({email_address}[^@<]+@[^<]+)|(({domain}[^\\\/<]+)[\\\/]+)?({user}[^<]+))<""",
    """<Client-IP-Address[^>]+>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Proxy-Policy-Name[^>]+>({additional_info}[^<]+)<""",
    """<Packet-Type[^>]+>({result}\d+)""",
    """<NAS-IP-Address data_type=[^>]+>({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})<"""
  ]
  DupFields = [ "host->dest_host","result->event_code" ]
  ParserVersion = "v1.0.0"


}
```