#### Parser Content
```Java
{
Name = "cyberark-pam-cef-user-switch-success-pwdretrieve"
Vendor = "CyberArk"
Product = "Cyberark Privilege Access Management"
TimeFormat = "epoch"
Conditions = [ """|Cyber-Ark|Vault|""", """act=Retrieve password""", """Safe""" ]
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF"""
"""({time}\w+\s+\d\d\s+\d\d:\d\d:\d\d)[^:]+CEF:"""
"""\srt=({time}\d{13})"""
"""\sdvc=({host}\S+?)(\s+\w+=|\s*$)"""
"""\sdvchost=({host}\S+?)(\s+\w+=|\s*$)"""
"""\sshost=(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^=]+?))(\s+\w+=|\s*$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser=(({domain}[^\\=]+?)(\\)+)?({user}.+?)\s+\w+="""
"""\sduser=([^\\=]+\\+)?({dest_user}[^=]+?)\s+\w+="""
"""cs2=(|({safe_value}[^=]+?))\s+\w+="""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdhost=({dest_host}[^=]+?)(\s+\w+=|\s*$)"""
]
DupFields = [ "dest_user->account" ]
ParserVersion = "v1.0.0"


}
```