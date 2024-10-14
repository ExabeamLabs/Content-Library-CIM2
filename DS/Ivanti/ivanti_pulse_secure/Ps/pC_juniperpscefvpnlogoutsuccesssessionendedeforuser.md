#### Parser Content
```Java
{
Name = "juniper-ps-cef-vpn-logout-success-sessionendedeforuser"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""VPN Tunneling: Session ended for user"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[^\s]+)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+sproc="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssproc=({realm}.+?)\s+spriv"""
"""\sspriv=({resource}.+?)\s+\w+="""
"""\sshost=({src_host}[^\s]+)"""
"""Session ended for user with IP(v4)? address ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```