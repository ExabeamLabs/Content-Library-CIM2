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
"""RemoteIP"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""Protocol"+:\s*"+({protocol}[^"]+)"""
"""LocalIP"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""LocalPort"+:({src_port}\d+)"""
"""ActionType\\?"+:\s*\\?"+({result}[^"]+?)\\?""""
"""RemoteIPType"+:\s*"+(null|({direction}[^"]+))"""
"""DeviceName\\?"+:\s*\\?"+({dest_host}[\w\-.]+?)\\?""""
"""InitiatingProcessAccountName\\?"+:\s*\\?"+(system|SYSTEM|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))\\?""""
""""ProcessIntegrityLevel\\?"+:\s*\\?"+({process_integrity}[^"]+?)\\?""""
"""InitiatingProcessAccountSid\\?"+:\s*\\?"+({user_sid}[^"]+?)\\?""""
"""InitiatingProcessFileName\\?"+:\s*\\?"+({process_name}[^"]+?)\\?""""
"""ProcessId\\?"+:({process_id}\d+)"""
""""FileName\\?"+:\s*\\?"+(|({process_name}[^"]+?))\\?,""""
""""InitiatingProcessCommandLine\\?"+:\s*\\?"\s*(|({process_command_line}.*?))\s*\\*",\s*""""
""""ProcessCommandLine\\?"+:\s*[\\"]*?"\s*(|({process_command_line}.*?))\s*[\\"]*",\s*""""
"""MD5\\?"+:\\?"+({hash_md5}[^"]+?)\\?""""
"""\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)"""
""""FolderPath"+:"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))""""
""""AccountDomain":"({domain}[^:]+?)",""",
""""InitiatingProcessFolderPath":\s*"({process_path}({process_dir}([^"]+)?[\\\/])?({process_name}[^\\\/"]+))""",
""""InitiatingProcessParentFileName":"({parent_process_name}[^"]+)""",
""""InitiatingProcessParentId"+:({parent_process_id}\d+)""",
""""SHA1":"({hash_sha1}[^"]+)"""",
""""InitiatingProcessSHA1":"({hash_sha1}[^"]+)"""",
""""SHA256":"({hash_sha256}[^",]+)",""",
""""InitiatingProcessSHA256":"({hash_sha256}[^",]+)",""",
""""InitiatingProcessVersionInfoProductName":"({product_name}[^"]+)""""
""""AccountName\\?"+:\s*\\?"+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
]
DupFields = [
"category->event_name"
"event_hub_namespace->host"
]
ParserVersion = "v1.0.0"


}
```