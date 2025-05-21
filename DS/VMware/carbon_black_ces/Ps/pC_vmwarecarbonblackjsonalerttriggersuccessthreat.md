#### Parser Content
```Java
{
Name = "vmware-carbonblack-json-alert-trigger-success-threat"
Vendor = "VMware"
Product = "Carbon Black CES"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""cb-defense"""
"""indicatorName"""
"""targetPriorityCode"""
"""targetPriorityType"""
"""threat"""
]
Fields = [
"""@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
""""externalIpAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""internalIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""deviceName":"(({domain}[^"\\]+)\\+)?({src_host}[^"]+)""""
"""deviceType":"({device_type}[^\\]+)""""
"""score"+:\s*({alert_severity}\d+)"""
"""agent.type":"({agent_name}[^"]+)""""
"""host":"({host}[^"]+)""""
"""type":"({threat_type}[^"]+)""""
"""incidentId":"({threat_id}[^"]+)""""
"""applicationName":"({process_name}[^"]+)""""
"""threatCategory":"({category}[^"]+)""""
"""indicatorName":"({alert_type}[^"]+)""""
"""ruleName":"({alert_name}[^"]+)""""
"""summary":"({additional_info}[^"]+)""""
"""email"+:\\s*"+(({domain}[^"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""deviceId"+:({sensor_id}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```