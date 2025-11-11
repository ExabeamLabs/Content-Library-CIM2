#### Parser Content
```Java
{
Name = microsoft-defenderep-sk4-process-create-success-processcreated
  Vendor = Microsoft
  Product = "Microsoft Defender"
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = ["""Invoke-WebRequest""", """AdvancedHunting-DeviceProcessEvents""", """ActionType""", """ProcessCreated""" ]
  Fields = [
     """time"+:\s*"+({time}[^"]+)"""",
     """operationName\\?"+:\s*\\?"+({operation}[^"]+?)\\?"""",
     """"category\\?"+:\s*\\?"+({event_name}({category}[^"]+?))\\?"""",
     """RemoteIP"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d).?\b){4}))(:({dest_port}\d+))?""",
     """"Protocol"+:\s*"+({protocol}[^"]+)""",
     """LocalIP"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d).?\b){4}))(:({src_port}\d+))?""",
     """LocalPort"+:({src_port}\d+)""",
     """ActionType\\?"+:\s*\\?"+({result}[^"]+?)\\?"""",
     """RemoteIPType"+:\s*"+(null|({direction}[^"]+))""",
     """DeviceName\\?"+:\s*\\?"+({dest_host}[\w\-.]+?)\\?"""",
     """DeviceId\\?"+:\s*\\?"+({device_id}[\w\.\-]+)\\?"""",
     """InitiatingProcessAccountName\\?"+:\s*\\?"+(system|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
     """"ProcessIntegrityLevel\\?"+:\s*\\?"+({process_integrity}[^"]+?)\\?"""",
     """InitiatingProcessAccountSid\\?"+:\s*\\?"+({user_sid}[^"]+?)\\?"""",
     """ProcessId\\?"+:({process_id}\d+)""",
     """InitiatingProcessFileName\\?"+:\s*\\?"+({process_name}[^"\\\/]+?)\\?"""",
     """"InitiatingProcessFolderPath"+:\s*"+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))""""
     """"FileName\\?"+:\s*\\?"+({process_name}[^"]+?)\\?,""""
     """"FolderPath"+:"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))"""",
     """"ProcessCommandLine\\?"+:\s*\\?"\s*({process_command_line}.+?)\s*\\*",""""
     """\"InitiatingProcessCommandLine\\?\"+:\s*\\?\"\s*({process_command_line}.+?)\s*\\*","\w+":"""
     """MD5\\?"+:\\?"+({hash_md5}[^"]+?)\\?"""",
     """\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)"""
     """"AccountDomain":"({domain}[^:]+?)",""",
     """Invoke-WebRequest\s*-Uri\s*'*({url}(\w+:\/{2})?({web_domain}[^\/\.\s]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx))+)?[^'\s]+)""",
     """"SHA1":"({hash_sha1}[^"]+)"""",
     """"InitiatingProcessSHA1":"({hash_sha1}[^"]+)"""",
     """"SHA256":"({hash_sha256}[^",]+)",""",
     """"InitiatingProcessSHA256":"({hash_sha256}[^",]+)",""",
     """"InitiatingProcessParentFileName":"({parent_process_path}({parent_process_dir}[^"]+[\\\/]+)?({parent_process_name}[^"\\\/]+))"""",
     """"InitiatingProcessVersionInfoProductName":"({product_name}[^"]+)""""
  ]


}
```