#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-malsite
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "epoch_sec"
  Conditions = [ """"alert_type":"malsite"""", """destinationServiceName =Netskope""", """"alert":"yes""" ]
  Fields = [
    """"timestamp":({time}\d{10})""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?))"""",
    """"app":"({process_path}[^"]+)""",
    """"dstip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"srcip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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
    """msg=.*?\[({alert_source}[^\]]+)\]:"""
    """"protocol":\s*"({protocol}[^"]+)""""
  ]
  DupFields = ["alert_type->threat_category"]


}
```