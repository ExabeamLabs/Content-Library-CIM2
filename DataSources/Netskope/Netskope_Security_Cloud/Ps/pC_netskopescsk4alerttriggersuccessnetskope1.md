#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-netskope-1
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"alert_type":"""", """destinationServiceName =Netskope""", """"ns_detection_name":"""",  ]
  Fields = [
    """"timestamp":({time}\d+)""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[^"@\\\/\s]+))"""",
    """"app":"({process_path}[^"]+)""",
    """"dstip":"({dest_ip}[A-Fa-f:\d.]+)""",
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
    """"local_sha256":"({shash_ha256_at}[^"]+)"""",
    """"site":"({site_at}[^"]+)""""
  ]
  DupFields = ["process_path->process_name"]


}
```