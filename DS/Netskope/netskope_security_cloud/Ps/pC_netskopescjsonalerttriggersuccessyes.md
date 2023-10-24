#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-yes
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  ParserVersion = "v1.0.0"
  Conditions = [ """"alert_type": "DLP"""", """"alert": "yes""""]
  Fields = [
    """"timestamp": ({time}\d{10})""",
    """"user": "(?![^\s]+@[^\s]+)({user}[\w\.\-]{1,40}\$?)"""",
    """"user": "(?=[^\s]+@[^\s]+)({email_address}[^"\s@]+@[^"\s@]+)"""",
    """"policy": "({alert_name}[^"]+)"""",
    """"alert_type": "({alert_type}[^"]+)"""",
    """"dstip": "({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"url": "({target}[^"]+)"""",
    """"shared_with": "({additional_info}[^"]+)"""",
    """"alert_name": "({alert_name}[^"]+)"""",
    """"internal_id": "({alert_id}[^"]+)"""",
    """"dlp_rule_severity": "({alert_severity}[^"]+)"""",
    """"dlp_file": "({file_name}[^"]+)"""",
    """"file_path": "({file_path}[^"]+)"""",
    """"md5":\s*"({hash_md5}[^"]+)"""",
    """"from_user":\s*"({from_user_at}[^"]+)"""",
    """"site":\s*"({site_at}[^"]+)""""
    """"protocol":\s*"({protocol}[^"]+)""""
    """"domain":"({web_domain}[^"]+)"""
    """"file_size":\s*({bytes}\d+)"""
    """"object":\s*"(\s+"|(\s*(Unknown Unknown|unknown|Unknown|null|({object}[^"]+?))\s*"))"""
  ]
  DupFields = [ "file_path->file_path_at", "additional_info->shared_with_at","alert_name"->"alert_subject" ]


}
```