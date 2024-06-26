#### Parser Content
```Java
{
Name = google-workspace-cef-app-activity-success-audit
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Google Workspace
  TimeFormat = ["epoch", "epoch_sec"]
  Conditions = [ """CEF:""", """destinationServiceName =Google Apps""", """cat=audit""", """dproc=Gmail Logs""" ]
  Fields = [
  """"timestamp_usec":({time}\d{10,13})""",
  """"destination":\[\{"address":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
  """"source":\{"address":"({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
  """"subject":"({email_subject}[^"]+)"""",
  """"selector":"({operation}[^"]+)""",
  """"success":({result}true|false)""",
  """"rfc2822_message_id":"({message_id}[^",]+)"""",
  """"payload_size":({bytes}\d+)""",
  """"client_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
  """({app}Gmail|gmail)""",
  """"action_type":({action_type}\d+)"""
  """"service":"({service_name}[^"]+)"""
  """suser=(anonymous|({email_address}[^@=\s]+@[^\.=\s]+\.[^=\s]+)|({user}[\w\.\-]{1,40}\$?))""",
  """"attachment":\[[^\}]+"file_name":"({email_attachment}[^\}]+?)"(,|\})"""
  ]
  DupFields = [ "src_email_address->email_address" ]


}
```