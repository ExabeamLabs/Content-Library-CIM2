#### Parser Content
```Java
{
Name = cloudflare-waf-sk4-network-traffic-success-fwnetworktraffic
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """requestClientApplication=""", """destinationServiceName =Cloudflare""", """dproc=Firewall""" , """cat=network-traffic"""]
  Fields = [
    """ext__occurred_at_=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"action":"({operation}[^"]+)"""",
    """suser=(anonymous|1|({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s)""",
    """"ua":"({user_agent}[^"]*?)"""",
    """"country":"({country_code}[^"]*?)"""",
    """deviceInboundInterface=({src_interface}.*?)\s*\w+=""",
    """dhost=({dest_host}.*?)\s+\w+=""",
    """dproc=({process_path}.*?)\s*\w+=""",
    """ext_proto=({protocol}.*?)\s*\w+=""",
    """reason=({failure_reason}.*?)\s*\w+=""",
    """deviceDirection=({direction}.*?)\s*\w+=""",
    """dpt=({dest_port}\d+)\s""",
    """spt=({src_port}\d+)\s""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """requestClientApplication=({app}.+?)\s*\w+=""",
    """"source":"({log_source}[^"]+?)"""",
    """\sin=\-?({bytes}\d+)\s*\w+=""",
    """ext_method=({method}[^\s]+)""",
    """cat=({category}[^\s]+)\s""",
    """cn2=({bytes}[^\s]+)\s""",
    """destinationServiceName =({dest_host}[^\s]+)\s"""
 ]


}
```