#### Parser Content
```Java
{
Name = "cimtrak-c-kv-file-read-success-filedeleted"
Conditions = [
"""CTK:"""
"""|Cimcor|CimTrak|"""
"""|File Deleted|"""
]
ParserVersion = "v1.0.0"
}  

{
    Name = bluecatnetworks-bnetworks-kv-dhcp-session-success-dhcpd
    Vendor = BlueCat Networks
    Product = BlueCat Networks
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """ dhcpd[""", """ DHCPIDENT:""", """| IP=""", """| Hostname=""" ]
    Fields = [
      """Hostname=(((?i)\[?None\]?)|({src_host}[^|]+?))\s*\|""",
      """MAC=({src_mac}[^\s]+?)\s+""",
      """IP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*\|""",
      """IP=[^|]+\|\s*({additional_info}[^"]+?)\s*("|$)""",
    ]
	ParserVersion = "v1.0.0"
 

}
```