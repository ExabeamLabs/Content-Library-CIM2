#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-alert-trigger-success-rulename"
Vendor = "SentinelOne"
Product = "Singularity Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
""""rulename":"""
""""activityType":"""
""""ruleid":"""
]
Fields = [
""""origagentname":\s*"({host}[^"]+)""""
""""createdAt":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""""
""""srcip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""dstip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""userName":\s*"({user}[\w\.\-]{1,40}\$?)""""
""""rulename":\s*"({alert_name}[^"]+)""""
""""dveventtype":\s*"({alert_type}[^"]+)""""
""""severity":\s*"({alert_severity}[^"]+)""""
""""sourceprocesscommandline":\s*"({process_command_line}[^,]+)","""
""""primaryDescription":\s*"({additional_info}[^"]+)""""
""""sourceprocessfilepath":\s*"({process_path}({process_dir}[^"]+)\\\\({process_name}[^"]+))""""
""""sourceparentprocesspath":\s*"({parent_process}[^"]+)""""
""""alertid":\s*({alert_id}[^"]+),"""
]
ParserVersion = "v1.0.0"


}
```