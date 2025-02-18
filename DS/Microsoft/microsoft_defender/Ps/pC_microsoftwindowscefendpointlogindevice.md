#### Parser Content
```Java
{
Name = "microsoft-windows-cef-endpoint-login-device"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Microsoft Defender"
ExtractionType = json
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
Conditions = [
""""DeviceName":"""
""""ActionType":"Logon"""
""""RemoteDeviceName":"""
""""category":"""
""""AdvancedHunting-DeviceLogonEvents""""
]
Fields = [
""""Timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""
""""DeviceName":"({host}[\w\-.]+)""""
""""AccountName":"(-|system|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))"+"""
""""AccountDomain":"({domain}[^"]+)""""
""""AccountSid":"({user_sid}[^"]+)""""
""""RemoteIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""RemotePort":({src_port}\d+)"""
""""Upn\\?":\\?"({email_address}[^"@\\\s]+@[^"@\\\s]+?)\\?""""
""""ActionType":"({result}[^"]+)""""
""""ActionType":"({result}LogonSuccess|LogonAttempted|LogonFailed)""""
""""InitiatingProcessFileName":"({process_name}[^"]+)""""
""""InitiatingProcessFolderPath":"({process_dir}[^"]+)""""
""""InitiatingProcessMD5":"({hash_md5}[^"]+)""""
""""InitiatingProcessId":({process_id}[^",]+)"""
""""InitiatingProcessCommandLine":"\s*({process_command_line}[^"]+)""""
""""LogonId":(null|({login_id}[^",]+))"""
""""DeviceId":"({device_id}[^"]+)""""
""""RemoteDeviceName":"(|({src_host}[\w\-.]+))""""
""""FailureReason":"({failure_reason}[^"]+)""""
"""exa_json_path=$..Timestamp,exa_field_name=time"""
"""exa_json_path=$..DeviceName,exa_field_name=host"""
"""exa_json_path=$..AccountName,exa_regex=(-|system|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?$)|({full_name}[^",]+))"""
"""exa_json_path=$..AccountDomain,exa_field_name=domain"""
"""exa_json_path=$..AccountSid,exa_field_name=user_sid,exa_match_expr=Contains($..AccountSid,"null")"""
"""exa_json_path=$..RemoteIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$..RemotePort,exa_field_name=src_port"""
"""exa_json_path=$..Upn,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""exa_json_path=$..ActionType,exa_field_name=result"""
"""exa_json_path=$..InitiatingProcessFileName,exa_field_name=process_name"""
"""exa_json_path=$..InitiatingProcessFolderPath,exa_field_name=process_dir"""
"""exa_json_path=$..InitiatingProcessMD5,exa_field_name=hash_md5"""
"""exa_json_path=$..InitiatingProcessId,exa_field_name=process_id"""
"""exa_json_path=$..InitiatingProcessCommandLine,exa_field_name=process_command_line"""
"""exa_json_path=$..LogonId,exa_field_name=login_id"""
"""exa_json_path=$..DeviceId,exa_field_name=device_id"""
"""exa_json_path=$.properties.RemoteDeviceName,exa_field_name=src_host"""
"""exa_json_path=$..FailureReason,exa_field_name=failure_reason"""
]


}
```