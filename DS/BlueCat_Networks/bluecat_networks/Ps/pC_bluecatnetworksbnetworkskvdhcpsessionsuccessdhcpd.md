#### Parser Content
```Java
{
Name = bluecatnetworks-bnetworks-kv-dhcp-session-success-dhcpd
    Vendor = BlueCat Networks
    Product = BlueCat Networks
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """ dhcpd[""", """ DHCPIDENT:""", """| IP=""", """| Hostname=""" ]
    Fields = [
      """Hostname=(((?i)\[?None\]?)|({src_host}[^|]+?))\s*\|""",
      """MAC=({src_mac}[^\s]+?)\s+""",
      """IP=({src_ip}[A-Fa-f0-9.:]+?)\s*\|""",
      """IP=[^|]+\|\s*({additional_info}[^"]+?)\s*("|$)""",
    ]
	ParserVersion = "v1.0.0"
 

}
```