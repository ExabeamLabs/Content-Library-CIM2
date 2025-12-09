#### Parser Content
```Java
{
Name = "delinea-secretserver-cef-user-switch-success-checkout"
Vendor = "Delinea"
Product = "Secret Server"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""|Thycotic Software|"""
"""|SECRET - CHECKOUT|"""
"""Item Name:"""
]
Fields = [
"""\d{2}:\d{2}:\d{2} ({dest_host}({host}[\w\-.]+)) CEF:"""
"""\srt=({time}\d+)"""
"""\srt=({time}\w+ \d{2} \d{4} \d{2}:\d{2}:\d{2})"""
"""\sdvc=({dest_host}({host}[^\s]+))"""
"""\sdvchost=({dest_host}({host}[^\s]+))"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser=(({domain}[^\\\s]+?)(\\+))?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\sfname=((({account_domain}({dest_domain}[^\\=\s]+))(\\)+)?({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({=account_domain}({=dest_domain}[^=\\]+))(\\+))?({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+="""
"""cs3=({safe_value}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```