#### Parser Content
```Java
{
Name = "cyberark-pam-cef-user-switch-success-pwdretrieve"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = ["epoch", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ"]
Conditions = [ """|Cyber-Ark|Vault|""", """act=Retrieve password""", """Safe""" ]
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF"""
"""({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)[^:]+CEF:"""
"""({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\dZ)[^:]+CEF:"""
"""\srt=({time}\d{13})"""
"""\sdvc=({host}\S+?)(\s+\w+=|\s*$)"""
"""\sdvchost=({host}\S+?)(\s+\w+=|\s*$)"""
"""\sshost=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^=]+?))(\s+\w+=|\s*$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser=(({domain}[^\\=]+?)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\sduser=([^\\=]+\\+)?({dest_user}[^=]+?)\s+\w+="""
"""cs2=(|({safe_value}[^=]+?))\s+\w+="""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdhost=({dest_host}[^=]+?)(\s+\w+=|\s*$)"""
"""CEF:\s*\d+\|([^\|]+\|){3}({event_code}[^\|]+)"""
"""CEF:\s*\d+\|([^\|]+\|){4}({event_name}[^\|]+)"""
"""CEF:\s*\d+\|([^\|]+\|){5}({severity}[^\|]+)"""
"""msg="*\[*({additional_info}[^"\]]+)?\]*\s*"""
"""act=({operation}Retrieve password)"""
"""cn2="*({action}[^=]+)\s"?(\s+\w+=)"""
"""cs3=({device_type}[^=]+)\s+\w+="""
]
DupFields = [ "dest_user->account" ]
ParserVersion = "v1.0.0"


}
```