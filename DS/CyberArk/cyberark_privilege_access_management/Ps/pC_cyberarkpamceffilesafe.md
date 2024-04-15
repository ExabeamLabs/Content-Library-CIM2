#### Parser Content
```Java
{
Name = "cyberark-pam-cef-file-safe"
Vendor = "CyberArk"
Product = "Cyberark Privilege Access Management"
TimeFormat = "epoch"
Conditions = [
"""CEF"""
"""|Cyber-Ark|Vault|"""
"""Safe"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
"""\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF"""
"""\srt=({time}\d{13})(\s+\w+=|\s*$)"""
"""\sdvc="?({host}[^"\s]+)"?(\s+\w+=|\s*$)"""
"""\sdvchost="?({host}[^"\s]+)"?(\s+\w+=|\s*$)"""
"""\ssrc="?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"?(\s+\w+=|\s*$)"""
"""shost="?(0.0.0.0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))"?(\s+\w+=|\s*$)"""
"""\sfname="?({domain}[^"\\]+)\\+[^"]+""""
"""\Wduser="?(|(({domain}[^\\="]+)(\\)+)?({user}[^"]+?))"?\s+(\w+=|$)"""
"""\ssuser="?(|(({domain}[^\\="]+)(\\)+)?({user}[^"]+?))"?(\s+\w+=|\s*$)"""
"""\sfname="?(|({src_file_path}({file_dir}[^="]*?[\\\/]+)?({src_file_name}[^="\\\/]+?(\.({src_file_ext}\w+))?)))"?(\s+\w+=|\s*$)"""
"""({file_type}(?i)file)"""
"""({app}Vault)"""
"""({protocol}SSH)""",
"""reason=?\s+cs1Label="?({process_command_line}[^\n"]+?)"""",
"""cs3="?({device_type}[^="]+?)"?\s+\w+""",
"""cs2="?({safe_name}[^="]+?)"?\s+\w+=""",
"""\Wact="?({operation}[^"=\[\]]+?)"?(\[|\]|\s+\w+=|\s*$)""",
"""fname=({additional_info}[^=]+?)\s+\w+="""
]
DupFields = [
"src_file_name->object"
"operation->access"
"src_file_name->file_name"
]
ParserVersion = "v1.0.0"


}
```