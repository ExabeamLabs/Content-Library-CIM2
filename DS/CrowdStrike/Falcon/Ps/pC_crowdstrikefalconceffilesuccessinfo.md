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
"""\"UserIp\":\s*\"({src_ip}[^\"]+)"""
"""\WdestinationServiceName =({app}.+?)\s+\w+="""
"""\"event_simpleName\":\"({event_code}[^\"]+)"""
"""\"aid\":\"({aid}[^\"]+)"""
"""\"(ImageFileName|TargetFileName)\":\"({src_file_path}[^\"]+)"""
"""\"(ImageFileName|TargetFileName)\":\"({file_dir}[^\"]*[\\\/]+)({src_file_name}[^\\\/\"]+\.({src_file_ext}[^\\\/\"]+))"""
"""\"UserName\":\"({user}[^\"]+?)\""""
"""\"aip\":\"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
"""\"ClientComputerName\":\"({src_host}[^\"]+)"""
"""\"id\":\"({alert_id}[\w-]+?)\""""
"""\"name\":\"({alert_name}[^\"]+?)\""""
"""\"File({access}Delete|Open|Rename)"""
]


}
```