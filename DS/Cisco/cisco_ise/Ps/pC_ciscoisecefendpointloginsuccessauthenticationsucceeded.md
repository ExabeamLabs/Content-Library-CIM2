#### Parser Content
```Java
{
Name = "cisco-ise-cef-endpoint-login-success-authenticationsucceeded"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "epoch"
Conditions = [
"""|Cisco|Cisco ISE|"""
"""Passed-Authentication: Authentication succeeded"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvc=({host}[A-Fa-f:\d.]+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wsuser=(({user_type}host)\/)?({user}[\w\.\-]{1,40}\$?)"""
"""\Wdhost=({dest_host}[\w\-.]+)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wcs6=Location#All Locations#AL#({location}[^,;]+)"""
"""\Wsource-ip\\=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wad\.NetworkDeviceName =({network}[^,\s]+)"""
]
DupFields = [
"dest_ip->auth_server"
"dest_host->computer_name"
]
ParserVersion = "v1.0.0"


}
```