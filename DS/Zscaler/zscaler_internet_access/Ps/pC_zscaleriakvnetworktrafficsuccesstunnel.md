#### Parser Content
```Java
{
Name = zscaler-ia-kv-network-traffic-success-tunnel
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = "v1.0.0"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [ """tunneltype=""", """sourceip=""", """IKE""", """Tunnel""" ]
  Fields = [
    """({time}\w+\s\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """datetime=({time}\w+\s\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """rxbytes=({bytes_in}\d+)\s+""",
    """txbytes=({bytes_out}\d+)\s+""",
    """srcport=({src_port}\d+)\s+""",
    """sourceip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """(destvip|destinationip)=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """tunneltype=({tunnel_type}[^=]+)\s+\w+=""",
    """location(name)?=({location}[^=]+)\s+""",
    """\sevent=({additional_info}[^=]+\s({status_msg}\w+))\s\w+=""",
    """(tunnelactionname|Recordtype)=({event_name}[^=]+?)\s\w+=""",
    """eventreason=(None|({result_reason}[^=]+?))\s*(\w+=|$)""",
    """(vpncredentialname|user)=((\d{1,3}\.){3}\d{1,3}|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
  ]
 

}
```