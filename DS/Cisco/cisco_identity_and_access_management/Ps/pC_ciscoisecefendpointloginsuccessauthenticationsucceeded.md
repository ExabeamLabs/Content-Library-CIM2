#### Parser Content
```Java
{
Name = "cisco-ise-cef-endpoint-login-success-authenticationsucceeded"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "epoch"
Conditions = [
"""|Cisco|Cisco ISE|"""
"""Passed-Authentication: Authentication succeeded"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvc=({host}[A-Fa-f:\d.]+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wsuser=((host\/)({src_host}[^,]+)|((::ffff:)?(?!(host\/)))?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|((([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|(({domain}[^\\\/,=]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))))"""
"""\Wdhost=({computer_name}({dest_host}[\w\-.]+))"""
"""\Wdst=({auth_server}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?"""
"""\Wcs6=Location#All Locations#AL#({location}[^,;]+)"""
"""\Wsource-ip\\=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wad\.NetworkDeviceName =({network}[^,\s]+)"""
]
ParserVersion = "v1.0.0"


}
```