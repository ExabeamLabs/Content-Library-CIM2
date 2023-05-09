#### Parser Content
```Java
{
Name = google-workspace-cef-app-activity-success-audit
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Google Workspace
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """destinationServiceName =Google Apps""", """cat=audit""", """dproc=Gmail Logs""" ]
  Fields = [
  """"timestamp_usec":({time}\d{13})""",
  """"destination":\[\{"address":"({dest_email_address}[^",]+)"""",
  """"source":\{"address":"({src_email_address}[^",]+)""",
  """"subject":"({email_subject}[^"]+)"""",
  """"selector":"({operation}[^"]+)""",
  """"success":({result}true|false)""",
  """"rfc2822_message_id":"({message_id}[^",]+)"""",
  """"payload_size":({bytes}\d+)""",
  """"client_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
  """({app}Gmail|gmail)""",
  """"action_type":({action_type}\d+)"""
  """"service":"({service_name}[^"]+)"""
  """suser=(anonymous|({user}[^\s]+))""",
  """"attachment":\[[^\}]+"file_name":"({email_attachment}[^\}]+?)"(,|\})"""
  ]
  DupFields = [ "src_email_address->email_address" ]


}
```