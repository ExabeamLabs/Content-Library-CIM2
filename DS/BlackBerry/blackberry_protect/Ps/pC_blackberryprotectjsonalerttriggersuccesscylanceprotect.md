#### Parser Content
```Java
{
Name = "blackberry-protect-json-alert-trigger-success-cylanceprotect"
Vendor = "BlackBerry"
Product = "BlackBerry Protect"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""src-application-name":"CylanceProtect""""
""""event-name":"""
""""source-device":"""
]
Fields = [
"""\d+\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)\s+[\w\-.]+\s+"""
""""event-name":"({alert_name}[^"]+)"""
""""event-name":"({alert_type}[^"]+)"""
""""classification":"({alert_type}[^"]+)"""
""""severity":({alert_severity}[^",]+)"""
""""file","name":"(|({file_path}({file_dir}[^"]*?)[\\\/]*({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\.\s"]+))?)))""""
""""source-device":\{[^\{\}]*?"name":"({dest_host}[\w\-.]+)"""
""""source-device":\{[^\{\}]*?"ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""source-device":\{[^\{\}]*?"mac-address":"({dest_mac}[^\s"]+)"""
""""hash-value":"({hash_sha256}[^"]+)"""
""""file_size":({bytes}\d+)"""
]
DupFields = [
"file_name->malware_file_name"
]
ParserVersion = "v1.0.0"


}
```