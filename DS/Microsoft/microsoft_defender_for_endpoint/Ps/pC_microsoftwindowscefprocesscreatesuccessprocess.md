#### Parser Content
```Java
{
Name = microsoft-windows-cef-process-create-success-process
ParserVersion = v1.0.0
Vendor = Microsoft
Product = Microsoft Defender for Endpoint
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""DeviceName":""",
""""ActionType":"ProcessCreated""""
]
Fields = [
""""Timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
"""DeviceName":\s*"({src_host}({host}[^"\.]+)?[^"]+)"""
""""AccountName":"(-|system|({user}[^"\s]+))""""
""""AccountDomain":"({domain}[^"\s]+)""""
""""AccountSid":"({user_sid}[^"]+)""""
""""ActionType":"({result}[^"]+)""""
""""FileName":"({process_name}[^"]+)""""
""""MD5":"({hash_md5}[^"]+)""""
""""ProcessId":({process_id}\d+)"""
""""ProcessCommandLine"+:"+\s*({process_command_line}.+?)\s*","FolderPath":"""
""""InitiatingProcessCommandLine"+:"+\s*({process_command_line}.+?)\s*","InitiatingProcessParentCreationTime":"""
""""FolderPath":"({process_path}({process_dir}[^"]*?[\\/]+)?({process_name}[^"\\/]+?))\s*""""
""""LogonId":({login_id}[^",]+)"""
""""DeviceId":"({device_id}[^"]+)""""
]


}
```