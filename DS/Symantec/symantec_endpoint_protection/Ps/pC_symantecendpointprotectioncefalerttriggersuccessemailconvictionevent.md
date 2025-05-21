#### Parser Content
```Java
{
Name = "symantec-endpointprotection-cef-alert-trigger-success-emailconvictionevent"
Vendor = "Symantec"
Product = "Symantec Endpoint Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""CEF:"""
"""|Symantec|"""
"""|email_conviction_event|"""
]
Fields = [
"""({host}[\w.\-]+)\s+email_conviction_event:"""
"""CEF:([^\|]*\|){5}({alert_type}[^\|]+)"""
""""device_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""\WinternalIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WinternalHost=({src_host}[^=]+?)(\s+\w+=|\s*$)"""
"""\Wmd5=({hash_md5}[^=]+?)(\s+\w+=|\s*$)"""
"""\Wuser_name=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)"""
""""threat":\{[^\}]*?"name":"({alert_name}[^"]+)"""
""""receivers":.*?"email_address":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))".*?"direction":"I""""
""""direction":"I".*?"receivers":.*?"email_address":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
""""sender":.*?"email_address":"({additional_info}[^"]+)".*?"direction":"I""""
""""direction":"I".*?"sender":.*?"email_address":"({additional_info}[^"]+)""""
""""email_action":"({action}[^"]+)"""
""""severity":({alert_severity}\d+)"""
""""file":.+?"name":"({malware_file_name}[^"]+)"""
""""sender_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```