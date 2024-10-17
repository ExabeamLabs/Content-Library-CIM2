#### Parser Content
```Java
{
Name = "cisco-asa-cef-vpn-logout-success-svcclosingconnection"
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
"""|CISCO|"""
"""|722037|SVC Closing Connection|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""({event_code}722037)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
"""\sduser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```