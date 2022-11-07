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
    """suser=({user}[^\s]+)\s""",
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
    """src=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """dst=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """requestClientApplication=({app}.+?)\s*\w+=""",
    """"source":"({log_source}[^"]+?)"""",
    """\sin=\-?({bytes}\d+)\s*\w+=""",
    """ext_method=({method}[^\s]+)""",
    """cat=({category}[^\s]+)\s""",
    """cn2=\-?({bytes}\d+)\s""",
    """destinationServiceName =({dest_host}[^\s]+)\s"""
 ]


}
```