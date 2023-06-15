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
    """"timestamp":({time}\d{10})""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[^"@\\\/\s]+))"""",
    """"app":"({app}[^"]+)""",
    """"dstip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"srcip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"_id":"({alert_id}[^"]+)""",
    """"category":"({threat_category}[^"]+)""",
    """"alert_name":"({alert_name}[^"]+)""",
    """"alert_type":"({alert_type}[^"]+)""",
    """"url":"({malware_url}[^"]+)""",
    """"risk_level":"({alert_severity}[^"]+)""",
    """"hostname":"({src_host}[^"]+)""",
    """"site":"({site_at}[^",]+)""""
  ]


}
```