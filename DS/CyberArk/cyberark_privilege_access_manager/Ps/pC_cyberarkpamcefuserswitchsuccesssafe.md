#### Parser Content
```Java
{
Name = "cyberark-pam-cef-user-switch-success-safe"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""|Cyber-Ark|Vault|"""
"""|Retrieve password|"""
"""Safe"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(z|Z)?"""
"""\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF:"""
"""\d\d:\d\d:\d\d ({dest_host}[\w\-.]+) CEF:"""
"""\sdvc="?({host}[^"\s]+?)"?(\s+\w+=|\s*$)"""
"""\sdvchost="?({host}[^"\s]+?)"?(\s+\w+=|\s*$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sshost="?(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))"?(\s+\w+=|\s*$)"""
"""\sfname="?({domain}[^"\\]+)\\+[^"]+"""
"""\ssuser="?(({domain}[^\\="]+?)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"?\s+\w+="""
"""\sfname=[^=]+?\-({dest_user}[^\s-]+?)\s+\w+="""
"""\sdhost="?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\:({dest_port}\d+))?|({dest_host}[\w\-.]+))"""
"""\sduser="?([^\\="]+\\+)?({dest_user}[^="]+?)"?\s+\w+="""
"""cs2="?({safe_value}[^"]+?)"?\s+\w+="""
"""CEF:\d+\|([^\|]+\|){3}({event_code}[^\|]+)"""
"""CEF:\d+\|([^\|]+\|){4}({event_name}[^\|]+)"""
"""CEF:\d+\|([^\|]+\|){5}({severity}[^\|]+)"""
"""msg="*\[*({additional_info}[^"\]]+)?\]*\s*"""
"""cn2="*({action}[^=]+)\s"+(\s+\w+=)"""
"""cs3="*({device_type}[^="]+)?"*\s+\w+="""
]
DupFields = [ "dest_user->account" ]
ParserVersion = "v1.0.0"


}
```