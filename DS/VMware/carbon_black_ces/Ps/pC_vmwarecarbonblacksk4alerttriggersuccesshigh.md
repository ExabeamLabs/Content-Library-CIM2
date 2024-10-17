#### Parser Content
```Java
{
Name = "vmware-carbonblack-sk4-alert-trigger-success-high"
Vendor = "VMware"
Product = "Carbon Black CES"
TimeFormat = "epoch"
Conditions = [
"""threatIndicators"""
"""targetPriorityType":"HIGH""""
""""shortDescription":""""
""""targetPriorityCode""""
""""processDetails":"""
]
Fields = [
""""eventTime":({time}\d{13})"""
""""deviceIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""deviceName":"(({domain}[^\\\s"]+)\\+)?({src_host}[^\\\s"]+)""""
""""email":"(({domain}[^\\\s"]+)\\+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
""""userName":"(({domain}[^\\\s"]+)\\+)?(SYSTEM|(?i)local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"=]+))""""
""""eventType":"({alert_name}[^"]+)""""
""""targetPriorityType":"({alert_severity}[^"]+)""""
""""eventType":"({alert_type}[^"]+)""""
"""threatIndicators":\[?"({alert_type}[^"]+)"""
""""commandLine":"({process_path}(({process_dir}[^"=,]+)\\)?({process_name}[^\s\\"]+))"""
""""peerFqdn":"({web_domain}[^"]+)""""
""""peerFqdn":"[^"\s]*?({top_domain}[^\/\.\s"]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za))+)"""
""""destAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""name":"({file_path}(\w:|\\\\)[^"]+)""""
""""name":"({file_dir}(\w:|\\\\)[^"]+?)\\+(?:[^\\="]+?)""""
""""name":"({file_path}(({file_dir}\w+:[^"]+?)\\+)?({file_name}[^"\\,:]+?(\.({file_ext}[^"]+))?))""""
""">({file_name}[^<"']+)<\/link><\/share>"*\s*was created by the application"""
]
ParserVersion = "v1.0.0"


}
```