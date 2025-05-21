#### Parser Content
```Java
{
Name = "microsoft-mdhcplog-str-dhcp-traffic-catchall"
 Conditions = [ """ DHCPLog: """ ]
 ParserVersion = v1.0.0

dhcplogs-events = {
    Vendor = "Microsoft"  
    Product = "Microsoft DHCP Log" 
    TimeFormat = ["MM/dd/yy,HH:mm:ss", "MMM dd HH:mm:ss"]
    Fields = [
      """,({time}\d\d\/\d\d\/\d\d,\d\d:\d\d:\d\d),({additional_info}[^,]+)?,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))?,({host}[\w\-.]+)?,({src_mac}[^,]+)?,"""
      """({time}\w\w\w \d\d \d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\sDHCPLog: ({event_code}\d[^\s]+)\s({additional_info}[^"]+)"""
      """({time}\w\w\w \d\d \d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\sDHCPLog: ({event_code}\d[^\s,]+),([^,]+,){2}({event_name}Conflict),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({additional_info}[^,]+)"""
    
}
```