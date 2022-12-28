#### Parser Content
```Java
{
Name = barracuda-firewall-kv-network-traffic-networktraffic
  ParserVersion = v1.0.0
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy MM dd HH:mm:ss"
  Conditions = [ """type=""", """|proto=""", """srcIF=""", """|dstService=""", """|dstIF=""", """|srcNAT=""", """|dstNAT=""" ]
  Fields = [
    """({time}\d+ \d+ \d+ \d+:\d+:\d+)""",
    """\s+({action}\w+):\s+type=""",
    """\s+type=({event_code}[^\|]+)\|proto=""",
    """proto=({protocol}[^\|]+)""",
    """srcIF=({src_interface}[^\|]+)""",
    """srcIP=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """srcPort=({src_port}\d+)""",
    """srcMAC=({src_mac}[^\|]+)""",
    """dstIP=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """dstPort=({dest_port}\d+)""",
    """dstIF=({dest_interface}[^\|]+)""",
    """rule=({rule}[^\|]+)""",
    """srcNAT=(0.0.0.0|({src_translated_ip}[^\|]+))""",
    """dstNAT=(0.0.0.0|({dest_external_ip}[^\|]+))""",
    """duration=({duration}[^\|]+)""",
    """receivedBytes=({bytes_in}\d+)""",
    """sentBytes=({bytes_out}\d+)""",
    """user=((NT AUTHORITY|({domain}[^\\]+))\\+)?(SYSTEM|({user}[^\|]+))""",
    """application=({app}[^\|]+)"""
   ]


}
```