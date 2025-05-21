#### Parser Content
```Java
{
Name = "vmware-carbonblack-sk4-file-write-success-cbdefense"
Vendor = "VMware"
Product = "Carbon Black CES"
TimeFormat = "epoch"
Conditions = [ """threatIndicators":""", """"eventType":"FILE_CREATE"""", """destinationServiceName =CB Defense""" ]
Fields = [
""""eventTime":({time}\d{13}),"""
""""deviceIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""deviceName":"(({domain}[^\\\s"]+)\\+)?({src_host}[^\\\s"]+)""""
""""email":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""""eventType":"({alert_name}[^"]+)""""
"""threatIndicators":\[?"({alert_type}[^"]+)"""
""""applicationPath":"({process_path}(({process_dir}[^"=,]+)\\)?({process_name}[^\\"]+))""""
""""applicationName":"({process_name}[^"]+)""""
""""targetPriorityType":"({alert_severity}[^"]+)""""
""""name":"({file_path}(\w:|\\\\)[^"]+)""""
""""name":"({file_dir}(\w:|\\\\)[^"]+?)\\+(?:[^\\="]+?)""""
""""name":"({file_path}(({file_dir}\w+:[^"]+?)\\+)?({file_name}[^"\\,:]+?(\.({file_ext}[^"]+))?))""""
""">({file_name}[^<"']+)<\/link><\/share>"*\s*was created by the application"""
]
ParserVersion = "v1.0.0"


}
```