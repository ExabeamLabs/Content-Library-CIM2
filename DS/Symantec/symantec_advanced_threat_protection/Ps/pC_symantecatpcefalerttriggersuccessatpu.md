#### Parser Content
```Java
{
Name = "symantec-atp-cef-alert-trigger-success-atpu"
Vendor = "Symantec"
Product = "Symantec Advanced Threat Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""|Symantec|ATPU|"""
"""|atp_incident|"""
""""events":"""
]
Fields = [
"""\Wdevice_time=({time}\d+\-\d+\-\d+T\d+:\d+:\d+\.\d+Z)"""
""""device_name":"({host}[^"]+)""""
""""events":\[.+?"signature_name":"({alert_name}[^"]+)".+?\]"""
""""events":\[.+?"threat":\{.*?"name":"({alert_name}[^"]+)".*?\}.+?\]"""
""""rule_name":"({alert_type}[^"]+)""""
""""events":\[.+?"alert":"({alert_type}[^"]+)".+?\]"""
""""events":\[.+?"file":\{.*?"md5":"?(?:null|({hash_md5}[^"]+))"?.*?\}.+?\]"""
""""events":\[.+?"file":\{.*?"folder":"({file_dir}[^"]+)".*?\}.+?\]"""
""""events":\[.+?"file":\{.*?"name":"({file_name}[^"]+)".*?\}.+?\]"""
""""events":\[.+?"email_subject":"({additional_info}[^"]+)".+?\]"""
""""events":\[.+?"incident_priority_level":"({alert_severity}[^"]+)".+?\]"""
""""events":\[.+?"user_name":"(?:SYSTEM|(A|a)dministrator|({full_name}[^\s"]+\s+[^\s"]+)|({user}[^"]+))".+?\]"""
""""events":\[.+?"sender":\{.*?"email_address":"({email_address}[^"]+)".*?\}.+?\]"""
""""events":\[.+?"device_name":"({src_host}[^"]+)".+?\]"""
""""events":\[.+?"device_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?".+?\]"""
""""events":\[.+?"email_action":"({action}[^"]+)".+?\]"""
""""events":\[.+?"actual_action":"({action}[^"]+)".+?\]"""
""""events":\[.+?"time":"({time}\d+\-\d+\-\d+T\d+:\d+:\d+\.\d+Z)".+?\]"""
""""atp_incident_id":({alert_id}\d+)"""
]
DupFields = [
"host->dest_host"
"file_name->process_name"
]
ParserVersion = "v1.0.0"


}
```