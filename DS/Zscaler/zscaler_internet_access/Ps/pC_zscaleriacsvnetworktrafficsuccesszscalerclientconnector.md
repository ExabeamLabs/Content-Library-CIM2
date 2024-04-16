#### Parser Content
```Java
{
Name = zscaler-ia-csv-network-traffic-success-zscalerclientconnector
  ParserVersion = "v1.0.0"
  Vendor = Zscaler
  Product = Zscaler Internet Access
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """"ZscalerClientConnector"""" ]
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""""
    """({action}(Allow|Drop))"""
    """"ZscalerClientConnector","({action}[^"]+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){1}"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){2}"({department}[^"]+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){3}"({location}[^"]+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){4}"({dest_port}\d+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){5}"({src_port}\d+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){8}"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){9}"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){19}"({service_name}[^"]+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){20}"({network_app}[^"]+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){21}"({protocol}[^"]+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){22}"({category}[^"]+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){25}"({rule}[^"]+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){26}"({bytes_in}\d+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){27}"({bytes_out}\d+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){28}"({duration}[^"]+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){30}"({session_id}[^"]+)""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){32}"(None|({threat_category}[^"]+))""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){34}"(None|({user}[\w\.\-]{1,40}\$?))""""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){35}"(NA|({src_host}[\w\-.]+))"""
      ]


}
```