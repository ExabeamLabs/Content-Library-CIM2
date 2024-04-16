#### Parser Content
```Java
{
Name = "microsoft-365defender-json-alert-trigger-success-publish"
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"category":"AdvancedHunting-AlertEvidence"""", """"operationName":"Publish"""", """"EntityType":""" ]
  Fields = [
    """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"hostname":"({host}[^"]+)"""",
    """"AlertId":"({alert_id}[^"]+)"""",
    """"EntityType":"({entity_type}[^"]+)""",
    """"FileName":"({file_name}[^"]+)""",
    """"FolderPath":"({file_path}[^"]+)""",
    """"DeviceName":"({src_host}[^"]+)""",
    """"SHA256":"({hash_sha256}[^"]+)""",
    """"SHA1":"({file_hash}[^"]+)""",
    """"DetectionStatus\\?":\\?"({result}[^"\\]+)""",
    """"AccountName":"(ALL|({user}[\w\.\-]{1,40}\$?))"""",
    """"AccountUpn":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"AccountSid":"({user_sid}[^"]+)""",
    """"EmailSubject":"({email_subject}[^"]+)""",
    """"Recipient\\?":\\?"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"Sender\\?":\\?"({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)""",
    """"SenderIP\\?":\\?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"RemoteIP\\?":\\?"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"Application\\?":\\?"({app}[^"]+)""",
    """"Urls\\?":\[\\?"({malware_url}[^\s,"]+)""",
    """"ProcessCommandLine":"({process_command_line}[^\n]+?)",""",
    """"Title":"({alert_name}[^"]+)"""",
    """"(C|c)ategory":"({alert_type}[^"]+)"""",
    """"Severity":"({alert_severity}[^"]+)"""",
    """"DetectionSource":"({alert_source}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```