#### Parser Content
```Java
{
Name = google-workspace-sk4-email-send-gmaillogs
  Vendor = Google
  Product = Google Workspace
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """destinationServiceName =Google Apps""", """"service":"smtp-outbound"""", """dproc=Gmail Logs""", """"action_type":""" ]
  Fields = [
  """"timestamp_usec":({time}\d{13})""",
  """"destination":\[\{"address[":]*({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
  """"source":\{"address[":]*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
  """"subject":"({email_subject}[^"]+)"""",
  """"selector":"({action}[^"]+)""",
  """"success":({result}true|false)""",
  """"rfc2822_message_id":"({message_id}[^"]+)"""",
  """"payload_size":({bytes}\d+)""",
  """"client_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
  """({app}Gmail|gmail)""",
  """num_message_attachments":({attachment_count}\d+)"""
  ]
  ParserVersion = v1.0.0


}
```