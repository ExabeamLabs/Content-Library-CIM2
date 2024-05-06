#### Parser Content
```Java
{
Name = "liquidfiles-l-json-app-activity-success-catchall"
Vendor = "LiquidFiles"
Product = "LiquidFiles"
Conditions = [
"""liquidfiles["""
""""message":""""
""""request_id":""""
]
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
""""hostname":"({host}[^"]+)""""
""""filename":"({file_name}[^"]+(\.)({file_ext}[^"]+))""""
""""ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""message":"({event_name}[^:"]+)"""
"""({app}liquidfiles)"""
""""username":"(({email_address}[^@"]+@[^\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?))""""
""""user_email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
"""user_group"+:"+({group_name}[^"]+)"""
""""email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
""""log_level":"({run_level}[^"]+?)\s*""""
""""error":"({failure_reason}[^"]+)""""
""""access_method":({method}[^"]+)""""
""""filename":"({file_name}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```