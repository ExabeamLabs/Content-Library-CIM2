#### Parser Content
```Java
{
Name = "cyberark-pam-cef-user-switch-success-psmconnect"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
ParserVersion = "v1.0.0"
TimeFormat = ["MMM dd HH:mm:ss"]
Conditions = [ """CEF:""", """|Cyber-Ark|Vault|""", """act="PSM Connect"""", """|PSM Connect|""", """suser=""", """duser=""" ]
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w\-\.]+) CEF"""
"""({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)[^:]+CEF:"""
"""\sdvc=({host}[\w\-\.]+?)(\s+\w+=|\s*$)"""
"""\sdvchost=({host}[\w\-\.]+?)(\s+\w+=|\s*$)"""
"""\sshost=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-\.]+?))(\s+\w+=|\s*$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser=(({domain}[^\\=]+?)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\sduser=(({dest_domain}[^\\=]+)[\\\/]+)?(({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+="""
"""cs2="*({safe_value}[^="]+?)"*\s+\w+="""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdhost=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-\.]+?))(\s+\w+=|\s*$)"""
"""\sduser=(({dest_domain}[^\\=]+)[\\\/]+)?({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
DupFields = [ "dest_user->account" ]


}
```