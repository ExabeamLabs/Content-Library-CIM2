#### Parser Content
```Java
{
Name = crowdstrike-falcon-cef-file-success-info
ParserVersion = "v1.0.0"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"File"""
"""Info""""
]
Fields = [
"""\"timestamp\":\s*\"*({time}\d{10})\""""
"""\"UserIp\":\s*\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WdestinationServiceName =({app}.+?)\s+\w+="""
""""destinationServiceName":"({app}.+?)"(\s+\w+=)?"""
"""\"event_simpleName\":\"({event_code}[^\"]+)"""
"""\"aid\":\"({aid}[^\"]+)"""
"""\"(ImageFileName|TargetFileName)\":\"({file_path}[^\"]+)"""
"""\"(ImageFileName|TargetFileName)\":\"({file_dir}[^\"]*[\\\/]+)({file_name}[^\\\/\"]+\.({file_ext}[^\\\/\"\.\-]+))"""
"""\"UserName\":\"({user}[^\"]+?)\""""
"""\"aip\":\"({aip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
"""\"ClientComputerName\":\"({src_host}[^\"]+)"""
"""\"id\":\"({alert_id}[\w-]+?)\""""
"""\"name\":\"({alert_name}[^\"]+?)\""""
"""\"File({access}Delete|Open|Rename)"""
]


}
```