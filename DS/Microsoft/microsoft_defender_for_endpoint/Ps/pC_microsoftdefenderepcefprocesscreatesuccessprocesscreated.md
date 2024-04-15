#### Parser Content
```Java
{
Name = "microsoft-defenderep-cef-process-create-success-processcreated"
Vendor = "Microsoft"
Product = "Microsoft Defender for Endpoint"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [
"""AdvancedHunting-DeviceProcessEvents"""
"""ActionType"""
"""ProcessCreated"""
]
Fields = [
"""time"+:\s*"+({time}[^"]+)""""
"""operationName\\?"+:\s*\\?"+({operation}[^"]+?)\\?""""
""""category\\?"+:\s*\\?"+({category}[^"]+?)\\?""""
"""RemoteIP"+:\s*"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""Protocol"+:\s*"+({protocol}[^"]+)"""
"""LocalIP"+:\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""LocalPort"+:({src_port}\d+)"""
"""ActionType\\?"+:\s*\\?"+({action}[^"]+?)\\?""""
"""RemoteIPType"+:\s*"+(null|({direction}[^"]+))"""
"""DeviceName\\?"+:\s*\\?"+({dest_host}[^"]+?)\\?""""
"""InitiatingProcessAccountName\\?"+:\s*\\?"+(system|SYSTEM|({user}[^"]+?))\\?""""
""""ProcessIntegrityLevel\\?"+:\s*\\?"+({process_integrity}[^"]+?)\\?""""
"""InitiatingProcessAccountSid\\?"+:\s*\\?"+({user_sid}[^"]+?)\\?""""
"""InitiatingProcessFileName\\?"+:\s*\\?"+({process_name}[^"]+?)\\?""""
"""ProcessId\\?"+:({process_id}\d+)"""
""""InitiatingProcessFolderPath"+:\s*"+({parent_process}({parent_process_dir}[^"]*[\\\/]+)?({parent_process_name}[^"\\\/]+))""""
"""InitiatingProcessFileName\\?"+:\s*\\?"+({parent_process_name}[^"\\\/]+)\\?"""",
""""FileName\\?"+:\s*\\?"+({process_name}[^"]+?)\\?""""
"""ProcessCommandLine\\?"+:\s*[\\"]*"\s*({process_command_line}[^"]+?)\s*\\*""""
""""InitiatingProcessCommandLine\\?"+:\s*\\?"\s*({process_command_line}.+?)\s*\\*",""""
"""MD5\\?"+:\\?"+({hash_md5}[^"]+?)\\?""""
"""\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)"""
""""FolderPath"+:"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))""""
""""AccountDomain":"({domain}[^:]+?)",""",
]
DupFields = [
"category->event_name"
"event_hub_namespace->host"
]
ParserVersion = "v1.0.0"


}
```