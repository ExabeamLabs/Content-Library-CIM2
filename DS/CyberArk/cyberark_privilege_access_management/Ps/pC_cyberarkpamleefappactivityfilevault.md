#### Parser Content
```Java
{
Name = "cyberark-pam-leef-appactivityfile-vault"
Vendor = "CyberArk"
Product = "Cyberark Privilege Access Management"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""LEEF:"""
"""|Cyber-Ark|Vault|"""
"""usrName ="""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s*({host}[\w\-.]+)\s*LEEF"""
"""(LEEF|CEF):([^\|]*?\|){4}({event_code}\d+)"""
"""\susrName =(({email_address}[^@]+@[^\s\.=]+\.[^\s\.=]+)|({user}[^=]+?)(@({domain}[^=]+))?)\s+\w+="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*"""
"""\s+File=({file_path}.+?)\s*\w+="""
"""\s+File=({file_dir}.+?)\\+[^\\]+\s*Location="""
"""\s+File=[^=]*\\({file_name}[^=]+?)\s*\w+="""
"""\s+File=[^=]*\\[^=]*\.({file_ext}[^=.\s\\]{1,100}?)\s*\w+="""
"""({file_type}(?i)file)"""
"""\s+File=({object}.+?)\s*Safe=({resource}.+?)\s*Location"""
"""Action=({operation}[^=]+?)\s*\w+="""
"""({app}Cyber-Ark)"""
"""ProcessName =({process_name}[^;=]+)"""
]
DupFields = [
"operation->access"
"operation->action"
]
ParserVersion = "v1.0.0"


}
```