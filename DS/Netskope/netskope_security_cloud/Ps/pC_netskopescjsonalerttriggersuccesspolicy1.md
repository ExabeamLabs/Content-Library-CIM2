#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-policy-1
  ParserVersion = v1.0.0
  Product = Netskope Security Cloud
  Conditions = [ """"alert_type":"policy"""",""""alert":"yes"""", """"alert_name":"""" ]

json-netskope-alert = {
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Fields = [
    """"timestamp":({time}\d{10})""",
    """"hostname":"({host}[\w\-.]+)"""",
    """"incident_id":({alert_id}\d+)""",
    """"srcip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"dstip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"dsthost":"({dest_host}[\w\-.]+)"""",
    """"alert_type":"({alert_type}[^"]+)"""",
    """"useragent":"({user_agent}[^"]+)"""",
    """"protocol":"({protocol}[^"]+)"""",
    """"user":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+))""",
    """"severity":"(unknown|({alert_severity}[^"]+))"""",
    """"numbytes":({bytes}\d+)""",
    """"page":"({web_domain}[^\\\/"]+)""",
    """"url":"({malware_url}[^"]+)"""
  ]
 DupFields = [ "alert_type->alert_name" 
}
```