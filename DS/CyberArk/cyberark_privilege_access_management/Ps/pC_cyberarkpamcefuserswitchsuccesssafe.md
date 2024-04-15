#### Parser Content
```Java
{
Name = "cyberark-pam-cef-user-switch-success-safe"
Vendor = "CyberArk"
Product = "Cyberark Privilege Access Management"
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
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sshost="?(0.0.0.0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))"?(\s+\w+=|\s*$)"""
"""\sfname="?({domain}[^"\\]+)\\+[^"]+"""
"""\ssuser="?(({domain}[^\\="]+?)(\\)+)?({user}[^"]+?)"?\s+\w+="""
"""\sfname=[^=]+?\-({dest_user}[^\s-]+?)\s+\w+="""
"""\sdhost="?(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\:({dest_port}\d+))?|({dest_host}[\w\-.]+))"""
"""\sduser="?([^\\="]+\\+)?({dest_user}[^="]+?)"?\s+\w+="""
"""cs2="?({safe_value}[^"]+?)"?\s+\w+="""
]
DupFields = [ "dest_user->account" ]
ParserVersion = "v1.0.0"


}
```