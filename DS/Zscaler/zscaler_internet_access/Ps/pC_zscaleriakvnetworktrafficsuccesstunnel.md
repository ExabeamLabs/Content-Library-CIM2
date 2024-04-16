#### Parser Content
```Java
{
Name = zscaler-ia-kv-network-traffic-success-tunnel
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = "v1.0.0"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [ """tunneltype=""", """vpncredentialname=""", """IKE""" ]
  Fields = [
    """datetime=({time}\w+\s\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """rxbytes=({bytes_in}\d+)\s+""",
    """txbytes=({bytes_out}\d+)\s+""",
    """srcport=({src_port}\d+)\s+""",
    """sourceip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """destvip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """tunneltype=({tunnel_type}[^=]+)\s+""",
    """locationname=({location}[^=]+)\s+""",
    """\sevent=({additional_info}[^=]+?tunnel is\s({status_msg}[^=]+?))\s\w+=""",
    """tunnelactionname=({event_name}[^=]+?)\s\w+=""",
    """eventreason=(None|({result_reason}[^=]+?))\s\w+=""",
    """vpncredentialname=((\d{1,3}\.){3}\d{1,3}|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?)))"""
  ]
 

}
```