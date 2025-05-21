#### Parser Content
```Java
{
Name = "symantec-atp-cef-alert-trigger-success-devicetime"
Vendor = "Symantec"
Product = "Symantec Advanced Threat Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""|Symantec|Symantec Advanced Threat Protection|"""
""""device_time":"""
]
Fields = [
"""CEF:([^\|]*\|){5}({alert_name}[^\|]+)"""
""""device_time":"({time}\d+\-\d+\-\d+T\d+:\d+:\d+\.\d+Z)"""
"""\Wdvchost=({host}.+?)(\s+\w+=|\s*$)"""
""""device_name":"({src_host}[^"]+)""""
""""device_domain":"({domain}[^"]+)""""
""""file":\{.*?"md5":"?(?:null|({hash_md5}[^"]+))""""
""""file":\{.*?"path":"({file_path}({file_dir}[^"]*?)({file_name}[^"\\\/]+?)(\.({file_ext}[^"\\\/.]+))?)""""
""""user_name":"(?:SYSTEM|(A|a)dministrator|({full_name}[^\s"]+\s+[^\s"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))".+?\]"""
""""device_os_name":"({os}[^"]+)""""
""""event_id":({alert_id}\d+)"""
""""severity_id":({alert_severity}\d+)"""
""""device_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""status_detail":"({alert_type}[^"]+)""""
""""product_name":"({product_name}[^"]+)""""
""""message":"({additional_info}[^"]+)""""
]
DupFields = [
"host->dest_host"
"file_name->process_name"
]
ParserVersion = "v1.0.0"


}
```