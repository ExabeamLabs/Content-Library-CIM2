#### Parser Content
```Java
{
Name = "cyberark-pam-cef-file-safe"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = ["epoch","yyyy-MM-dd'T'HH:mm:ssZ", "MMM dd HH:mm:ss"]
Conditions = [
"""CEF"""
"""|Cyber-Ark|Vault|"""
"""Safe"""
]
Fields = [
"""({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)[^:]+CEF:"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
"""\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF"""
"""\srt=({time}\d{13})(\s+\w+=|\s*$)"""
"""\sdvc="?({host}[^"\s]+)"?(\s+\w+=|\s*$)"""
"""\sdvchost="?({host}[^"\s]+)"?(\s+\w+=|\s*$)"""
"""\ssrc="?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"?(\s+\w+=|\s*$)"""
"""shost="?(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))"?(\s+\w+=|\s*$)""",
"""dhost="?(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))"?(\s+\w+=|\s*$)""",
"""\sfname="?({domain}[^"\\]+)\\+[^"]+""""
"""\Wduser="?(|(({dest_domain}[^\\="]+)(\\)+)?({dest_user}[\w\.\-]{1,40}\$?))"?\s+(\w+=|$)"""
"""\ssuser="?(|(({domain}[^\\="]+)(\\)+)?({user}[\w\.\-]{1,40}\$?))"?(\s+\w+=|\s*$)"""
"""\sfname="?(|({src_file_path}({file_dir}[^="]*?[\\\/]+)?({src_file_name}[^="\\\/]+?(\.({src_file_ext}\w+))?)))"?(\s+\w+=|\s*$)"""
"""({file_type}(?i)file)"""
"""({app}Vault)"""
"""({protocol}SSH)""",
"""reason=?\s+cs1Label="?({process_command_line}[^\n"]+?)"""",
"""reason="?({result_reason}[^="]+?)"?\s+\w+=""",
"""cs3="?({device_type}[^="]+?)"?\s+\w+""",
"""cs2="?({safe_name}[^="]+?)"?\s+\w+=""",
"""\Wact="?({operation}[^"=\[\]]+?)"?(\[|\]|\s+\w+=|\s*$)""",
"""fname=({additional_info}[^=]+?)\s+\w+=""",
"""Error:\s*({failure_reason}[^:]+?)\s*\w+:""",
"""(C|c)ode:\s*({failure_code}\d+),"""
]
DupFields = [
"src_file_name->object"
"operation->access"
"src_file_name->file_name"
]
ParserVersion = "v1.0.0"


}
```