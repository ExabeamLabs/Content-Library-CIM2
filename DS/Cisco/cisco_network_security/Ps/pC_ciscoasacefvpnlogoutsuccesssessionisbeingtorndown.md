#### Parser Content
```Java
{
Name = "cisco-asa-cef-vpn-logout-success-sessionisbeingtorndown"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|CISCO|ASA"""
"""|Session is being torn down|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdst=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```