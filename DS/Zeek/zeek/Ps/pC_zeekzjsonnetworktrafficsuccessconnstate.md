#### Parser Content
```Java
{
Name = zeek-z-json-network-traffic-success-connstate
  Vendor = Zeek
  Product = Zeek
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ 
""""id.orig_h"""
""""id.resp_h"""
""""conn_state"""
""""orig_pkts"""
]
  Fields = [
    """\"ts\\?\"+:[\[]*\"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """\"uid\\?\"+:\\?\"+({connection_id}[^\"]+)""",
    """\"id\.orig_h\\?\"+:\\?\"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\"id\.orig_p\\?\"+:({src_port}\d+)""",
    """\"id\.resp_h\\?\"+:\\?\"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\"id\.resp_p\\?\"+:({dest_port}\d+)""",
    """\"proto\\?\"+:\\?\"+({protocol}[^"]+)""",
    """\"orig_ip_bytes\\?\"+:({bytes_in}\d+)""",
    """\"resp_ip_bytes\\?\"+:({bytes_out}\d+)""",
    """\"sensorname\\?\"+:\\?\"+({sensor_name}[^"]+)""",
    """\"orig_pkts\":\s*({orig_pkts}\d+)""",
    """\"resp_pkts\":\s*({resp_pkts}\d+)""",
    """\"orig_cc\":\"({country}[^"]+)""",
    """\"service\":\"({operation}[^"]+)"""
]


}
```