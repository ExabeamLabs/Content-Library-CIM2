#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-alerttypeanomaly
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "epoch_sec"
  Conditions = [ """"alert_type":"anomaly"""", """destinationServiceName =Netskope""" ]
  Fields = [
    """"timestamp":({time}\d+)""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[^"@\\\/\s]+))"""",
    """"app":"({process_name}[^"]+)""",
    """"dstip":"({dest_ip}[A-Fa-f:\d.]+)""",
    """"srcip":"({src_ip}[A-Fa-f:\d.]+)""",
    """"_id":"({alert_id}[^"]+)""",
    """"category":"({threat_category}[^"]+)""",
    """"alert_name":"({alert_name}[^"]+)""",
    """"alert_type":"({alert_type}[^"]+)""",
    """"url":"({malware_url}[^"]+)""",
    """"risk_level":"({alert_severity}[^"]+)""",
    """"hostname":"({src_host}[^"]+)""",
    """"site":"({site_at}[^",]+)""""
  ]
  DupFields = ["site_at->app"]


}
```