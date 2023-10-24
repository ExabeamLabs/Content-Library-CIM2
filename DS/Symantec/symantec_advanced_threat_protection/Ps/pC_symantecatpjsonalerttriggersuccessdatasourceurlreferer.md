#### Parser Content
```Java
{
Name = "symantec-atp-json-alert-trigger-success-datasourceurlreferer"
Vendor = "Symantec"
Product = "Symantec Advanced Threat Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""product_name":"SymantecEDR:Endpoint"""
"""downloaded_portal_id""""
"""data_source_url_referer"""
]
Fields = [
""""device_time":"({time}[^"]+)""""
""""user_name":"({user}[\w\.\-]{1,40}\$?)""""
""""device_name":"({host}[^"]+)""""
""""host_name":"({src_host}[^"]+)""""
""""domain_name":"({domain}[^"]+)""""
""""device_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""data_source_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""folder":"({file_path}[^"]+)""""
""""data_source_url":"({malware_url}[^"]+)""""
""""name":"({file_name}[^"]+)""""
]
DupFields = [
"file_name -> alert_name"
]
ParserVersion = "v1.0.0"


}
```