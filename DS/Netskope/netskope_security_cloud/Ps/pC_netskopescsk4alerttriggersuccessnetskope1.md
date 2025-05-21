#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-netskope-1
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"alert_type":""", """"ccl":""", """"ns_detection_name":""", """"alert":""", """"yes"""" ]
  Fields = [
    """"timestamp":({time}\d{10})""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?))"""",
    """"app":"({app}[^"]+)""",
    """"dstip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"malware_id":"({alert_id}[^"]+)""",
    """"category":"({threat_category}[^"]+)""",
    """"ns_detection_name":"({alert_name}[^"]+)""",
    """"alert_type":"({alert_type}[^"]+)""",
    """"url":"({malware_url}[^"]+)""",
    """"malware_scanner_result":"({action}[^"]+)""",
    """"local_md5":"({hash_md5}[^"]+)""",
    """"malware_severity":"({alert_severity}[^"]+)""",
    """"file_path":"({file_path_at}[^"]+)"""",
    """"shared_with":\[({shared_with_at}[^\]]+)\]""",
    """"local_sha256":"({hash_sha256_at}[^"]+)"""",
    """"site":"({site_at}[^"]+)""""
  ]
  DupFields = ["process_path->process_name"]


}
```