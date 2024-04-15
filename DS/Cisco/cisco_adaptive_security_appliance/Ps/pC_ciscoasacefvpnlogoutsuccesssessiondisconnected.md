#### Parser Content
```Java
{
Name = "cisco-asa-cef-vpn-logout-success-sessiondisconnected"
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
"""|CISCO|"""
"""|113019|Session disconnected|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sduser=({full_name}(\w+\s+)+\w+)\s+(\w+=|$)"""
"""\sduser=({user}[^\s@]+)\s+(\w+=|$)"""
"""\sduser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}.+?)\s+(\w+=|$)"""
"""\scs6=[^=]*?({session_hour}\d+)h:({session_min}\d+)m:({session_sec}\d+)s"""
"""\sin=({bytes_in}\d+)"""
"""\sout=({bytes_out}\d+)"""
]
ParserVersion = "v1.0.0"


}
```