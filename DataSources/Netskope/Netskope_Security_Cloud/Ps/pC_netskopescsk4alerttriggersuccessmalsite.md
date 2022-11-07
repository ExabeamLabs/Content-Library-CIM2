#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-malsite
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "epoch_sec"
  Conditions = [ """"alert_type":"malsite"""", """destinationServiceName =Netskope""" ]
  Fields = [
    """"timestamp":({time}\d+)""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[^"@\\\/\s]+))"""",
    """"app":"({process_path}[^"]+)""",
    """"dstip":"({dest_ip}[A-Fa-f:\d.]+)""",
    """"srcip":"({src_ip}[A-Fa-f:\d.]+)""",
    """"malsite_category":\["({alert_type}[^"]+)"[^\]]*?\]""",
    """"alert_name":"({malware_url}[^"]+)""",
    """dpriv=({alert_name}[^=]+)\s+\w+=""",
    """"alert_type":"({alert_name}[^"]+)""",
    """"action":"({action}[^"]+)""",
    """"severity_level":"({alert_severity}[^"]+)""",
    """"hostname":"({src_host}[^"]+)""",
    """"referer":"({referrer}[^"]+)""",
    """"url":"({url}(\w+:\/+)?({web_domain}[^\\\/]+)[^"]+)""",
    """"browser":"({process_path}[^"]+)"""",
    """"site":"({site_at}[^",]+)"""",
    """"_id":"({alert_id}[^"]+)"""
  ]
  DupFields = ["alert_type->threat_category"]


}
```