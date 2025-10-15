#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-file-write-success-modifyservicebinary"
ParserVersion = "v1.0.0"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch"
Conditions = [
""""event_simpleName":"""
"""ModifyServiceBinary"""
]
Fields = [
""""timestamp":\s*"*({time}\d{13})"""",
"""\"UserIp\":\s*\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WdestinationServiceName =({app}.+?)\s+\w+="""
""""destinationServiceName":"({app}.+?)"(\s+\w+=)?"""
"""\"event_simpleName\":\"({event_code}[^\"]+)"""
"""\"aid\":\"({aid}[^\"]+)"""
"""\"(ImageFileName|TargetFileName)\":\"({file_path}({src_file_path}[^\"]+))"""
"""\"(ImageFileName|TargetFileName)\":\"({file_dir}[^\"]*[\\\/]+)({file_name}({src_file_name}[^\\\/\"]+\.({file_ext}({src_file_ext}[^\\\/\"]+))))"""
"""\"UserName\":\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
"""\"aip\":\"({aip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
"""\"ClientComputerName\":\"({src_host}[^\"]+)"""
"""\"ServiceImagePath\":\"({file_path}({src_file_path}({file_dir}[^\"]*?\\+)({file_name}({src_file_name}[^\\\s\"]+?\.({file_ext}({src_file_ext}[^\\\s\"\.]+?))))))(\s|\")"""
"""\"ServiceObjectName\":\"({additional_info}[^\"]+)"""
"""({action}ModifyServiceBinaryV2)"""
""""cid":"({cid}[^"]+)"""
""""event_platform":"({os}[^"]+)""""
]


}
```