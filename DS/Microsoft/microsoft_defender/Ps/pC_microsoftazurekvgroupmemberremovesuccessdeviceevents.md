#### Parser Content
```Java
{
Name = "microsoft-azure-kv-group-member-remove-success-deviceevents"
Conditions = [
"""|beatname=eventhubbeat|"""
"""|device_type=eventhubbeat|"""
"""|subject=AdvancedHunting-DeviceEvents|"""
"""vmid="""
"""@timestamp"""
"""@metadata"""
""""ActionType":"UserAccountRemovedFromLocalGroup""""
]
Vendor = "Microsoft"
Product = "Microsoft Defender"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
"""@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""
"""\d+-\d+-\d\dT\d+:\s\d+:\d+\.\d+\+\d+\s({host}[^\s]+)"""
"""subject=({event_name}[^|\s]+)"""
"""category":"({category}[^"]+)"""
"""ActionType":"({operation}[^"]+)"""
"""DeviceName":"({dest_host}[\w\-.]+)"""
""""FileName":"({file_name}[^"]+)"""
""""FolderPath":"({file_path}[^"]+)"""
""""InitiatingProcessAccountDomain":"({domain}[^"]+)"""
""""InitiatingProcessAccountName":"(system|SYSTEM|NETWORK SERVICE|local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
""""InitiatingProcessAccountSid":"({user_sid}[^"]+)"""
""""InitiatingProcessCommandLine":"\s*({process_command_line}.+?)\s*"+\,"""
""""InitiatingProcessFileName":"({process_name}[^"]+)"""
""""InitiatingProcessFolderPath":"({process_dir}[^"]+)"""
""""InitiatingProcessParentFileName":"({parent_process_name}[^"]+)"""
""""InitiatingProcessIntegrityLevel":"({process_integrity}[^"]+)"""
""""MD5":"({hash_md5}[^"]+)"""
""""InitiatingProcessId":({process_id}\d+)"""
""""LogonId"+:({login_id}\d+)"""
""""AccountName"+:"+({group_name}[^"]+)"""
""""AccountDomain"+:"+({group_domain}[^"]+)"""
""""AccountSid"+:"+({user_sid}[^"]+)"""
""""MemberSid\\"+:\\"+(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[^"]+))"""
]
ParserVersion = "v1.0.0"


}
```