#### Parser Content
```Java
{
Name = zscaler-fwzc-kv-network-traffic-success-cloud
  ParserVersion = v1.0.0
  Vendor = Zscaler
  Product = FW Zscaler Cloud
  TimeFormat = ["EEE MMM dd HH:mm:ss yyyy","EEE MMM  d HH:mm:ss yyyy"]
  Conditions = [ """orig=FW Zscaler Cloud|""" , """|datetime=""", """|action=""", """|rule=""", """|durationms=""" ]
  Fields = [
    """\|datetime=({time}\w\w\w \w\w\w\s*\d+\s*\d\d:\d\d:\d\d \d\d\d\d)"""
    """\|user=((\w+_)[^"\|]+|({user}\w+))"""
    """\|location=({location}[^\=]+?)\s+\w+="""
    """\|department=({department}[^\=]+?)\s+\w+="""
    """\|dest_port=({dest_port}\d+)"""
    """\|src_port=({src_port}\d+)"""
    """\|sip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\|dip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\|action=({action}\w+)"""
    """\|nwapp=({network_app}[^\|]+?)\|""",
    """\|protocol=({protocol}[^\|])\s+\|""",
    """\|bytes_in=({bytes_in}\d+)\|"""
    """\|bytes_out=({bytes_out}\d+)\|"""
    """\|durationms=({duration}\d+)\|"""
    """\|service_id=({service_id}[^\|]+)\|"""
    """\|rule=(rule}[^\|]+)\|"""
    """\|tuntype=({tunnel_protocol}[^\|]+?)\|"""
    """\|destcountry=({dest_country}[^\|]+?)\|"""
  ]
 

}
```