#### Parser Content
```Java
{
Name = "tanium-ep-json-alert-trigger-success-accountenumeration"
Product = "Tanium Threat Response"
Vendor = "Tanium"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Intel Id"""
"""Intel Type"""
"""Intel Name"""
"""Intel Labels"""
"""recorder_unique_id"""
""""type""""
""""process""""
]
Fields = [
""""+Alert Id"+:"+({alert_id}[^"]+)"""
""""+Timestamp"+:"+({time}[^"]+)"""
""""+Computer Name"+:"+({host}[^".]+)"""
""""+Computer IP"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""+Intel Type"+:"+({alert_type}[^"]+)"""
""""+Intel Name"+:"+({alert_name}[^"]+)"""
""""properties"+:[^\]]+?fullpath"+:"+({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+))""",
""""properties\\?"+:[^\]]+?md5\\?"+:\\?"+({hash_md5}[^"]+?)\\?"""",
""""properties\\?"+:[^\]]+?args\\?"+:"*\\*"+({process_command_line}[^,\]]+?)\\?\s*","cwd""",
""""user"+:"+(?:(?:NT AUTHORITY|({domain}[^\\"]+))\\+)?(?:SYSTEM|LOCAL SERVICE|({user}[\w\.\-]{1,40}\$?))"+\}\,"+source"+:"""
""""os"+:"+({os}[^"]+)"""
]
DupFields = [
"process_path->path"
]
ParserVersion = "v1.0.0"


}
```