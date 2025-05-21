#### Parser Content
```Java
{
Name = barracuda-firewall-kv-network-traffic-firewallactivity
  Vendor = "Barracuda"
  Product = "Barracuda Cloudgen Firewall"
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """/box_Firewall_Activity: """, """|user=""", """|proto=""", """|srcIP=""" ]
  Fields = [
    """({time}\w{3}\s+\d\d\s+\d\d:\d\d:\d\d)\s""",
    """\/box_Firewall_Activity:(\s+[-+][\d:\d]+)?\s+\w+\s+({host}[\w\-.]+)\s+({action}[^\s:]+):\s+({event_code}[^\|\s]+)\|""",
    """\|proto=({protocol}[^\|]+)\|""",
    """\|srcIF=({src_interface}[^\|]+)\|""",
    """\|srcIP=(?:0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\|""",
    """\|srcPort=({src_port}\d+)\|""",
    """\|srcMAC=({src_mac}[^\|]+)\|""",
    """\|dstIP=(?:0.0.0.0|({dest_external_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\|""",
    """\|dstPort=({dest_port}\d+)\|""",
    """\|dstService=({app_protocol}[^\|]+)\|""",
    """\|dstIF=({dest_interface}[^\|]+)\|""",
    """\|rule=({rule}[^\|]+)\|""",
    """\|info=({result_code}[^\|]+)\|""",
    """\|srcNAT=(?:0.0.0.0|({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
    """\|dstNAT=(?:0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\|""",
    """\|duration=({duration}\d+)""",
    """\|receivedBytes=({bytes_in}\d+)""",
    """\|sentBytes=({bytes_out}\d+)""",
    """\|user=(-|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\|"""
  ]
  ParserVersion = "v1.0.0"


}
```