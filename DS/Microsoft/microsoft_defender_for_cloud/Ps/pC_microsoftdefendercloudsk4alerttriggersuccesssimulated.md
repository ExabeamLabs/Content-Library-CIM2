#### Parser Content
```Java
{
Name = microsoft-defendercloud-sk4-alert-trigger-success-simulated
  Vendor = Microsoft
  Product = Microsoft Defender for Cloud
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """CEF:""", """"VendorName":"Microsoft"""", """"AlertType":"SIMULATED""", """"Type":"""" ]
  Fields=[
  """"TimeGenerated":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,7}Z)"""
  """"Severity":"({alert_severity}[^"]+)""",
  """"SystemAlertId":"({alert_id}[^"]+)""",
  """"Description":"\s*({additional_info}[^"]+?)\s*"""",
  """"AlertType":"({alert_type}[^"]+)""",
  """"AlertDisplayName":"({alert_name}[^"]+?)\s*""",
  """"CompromisedEntity":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({src_host}[\w\-\.]+))"""
  """"User Name":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\"]+)\\{1,100})?({user}[\w\.\-]{1,40}\$?))""""
  """"AlertUri":"({malware_url}[^"]+)"""
  """"Compromised Host":"({host}[\w\-\.]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```