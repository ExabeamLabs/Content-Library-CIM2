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
    """"timestamp": ({time}\d+)""",
    """"user": "(?![^\s]+@[^\s]+)({user}[^"\s]+)"""",
    """"user": "(?=[^\s]+@[^\s]+)({email_address}[^"\s@]+@[^"\s@]+)"""",
    """"policy": "({alert_name}[^"]+)"""",
    """"alert_type": "({alert_type}[^"]+)"""",
    """"dstip": "({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
    """"url": "({target}[^"]+)"""",
    """"shared_with": "({additional_info}[^"]+)"""",
    """"alert_name": "({alert_name}[^"]+)"""",
    """"internal_id": "({alert_id}[^"]+)"""",
    """"dlp_rule_severity": "({alert_severity}[^"]+)"""",
    """"dlp_file": "({file_name}[^"]+)"""",
    """"file_path": "({file_path}[^"]+)"""",
    """"file_size": ({bytes}\d+),""",
    """"md5":\s*"({hash_md5}[^"]+)"""",
    """"from_user":\s*"({from_user_at}[^"]+)"""",
    """"site":\s*"({site_at}[^"]+)""""
  ]
  DupFields = [ "file_path->file_path_at", "additional_info->shared_with_at" ]


}
```