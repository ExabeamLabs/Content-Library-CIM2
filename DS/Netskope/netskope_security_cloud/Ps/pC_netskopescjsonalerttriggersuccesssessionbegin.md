#### Parser Content
```Java
{
Name = "netskope-sc-json-alert-trigger-success-sessionbegin"
Vendor = "Netskope"
Product = "Netskope Security Cloud"
TimeFormat = "epoch_sec"
Conditions = [
"""session_begin"""
""""alert": "yes""""
]
Fields = [
""""dstip": "({host}[^"]+)","""
""""timestamp": ({time}\d{10})"""
""""user": "(?![^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
""""user": "(?=[^\s]+@[^\s]+)({email_address}[^"\s@]+@[^"\s@]+)""""
""""policy": "({alert_name}[^"]+).*({alert_type}policy)"""
""""alert_name": "({alert_name}[^"]+)""""
""""alert_type": "({alert_type}[^"]+)""""
""""dstip": "({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""srcip": "({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""url": "({additional_info}[^"]+)""""
""""app":\s*"({process_name}[^"]+)""""
""""from_user":\s*"({from_user_at}[^"]+)""""
""""shared_with":\s*"({shared_with_at}[^"]+)""""
""""site":\s*"({site_at}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```