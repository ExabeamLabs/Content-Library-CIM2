#### Parser Content
```Java
{
Name = "microsoft-windows-cef-endpoint-login-device"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Microsoft Defender for Endpoint"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""DeviceName":"""
""""ActionType":"Logon"""
""""RemoteDeviceName":"""
]
Fields = [
""""Timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
""""DeviceName":"({host}[\w\-.]+)""""
""""AccountName":"(-|system|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
""""AccountDomain":"({domain}[^"\s]+)""""
""""AccountSid":"({user_sid}[^"]+)""""
""""RemoteIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""RemotePort":({src_port}\d+)"""
""""Upn\\?":\\?"({email_address}[^"@\\\s]+@[^"@\\\s]+?)\\?""""
""""ActionType":"({result}[^"]+)""""
""""InitiatingProcessFileName":"({process_name}[^"]+)""""
""""InitiatingProcessFolderPath":"({process_dir}[^"]+)""""
""""InitiatingProcessMD5":"({hash_md5}[^"]+)""""
""""InitiatingProcessId":({process_id}[^",]+)"""
""""InitiatingProcessCommandLine":"\s*({process_command_line}[^"]+)""""
""""LogonId":(null|({login_id}[^",]+))"""
""""DeviceId":"({device_id}[^"]+)""""
""""RemoteDeviceName":"(|({src_host}[\w\-.]+))""""
""""FailureReason":"({failure_reason}[^"]+)""""
]


}
```