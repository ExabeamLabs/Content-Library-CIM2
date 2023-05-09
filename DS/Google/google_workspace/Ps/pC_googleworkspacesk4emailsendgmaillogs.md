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
  """"destination":\[\{"address[":]*({dest_email_address}[^",]+)"""",
  """"source":\{"address[":]*({src_email_address}[^",]+)""",
  """"subject":"({email_subject}[^"]+)"""",
  """"selector":"({action}[^"]+)""",
  """"success":({result}true|false)""",
  """"rfc2822_message_id":"({message_id}[^"]+)"""",
  """"payload_size":({bytes}\d+)""",
  """"client_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
  """({app}Gmail|gmail)""",
  """num_message_attachments":({num_attachments}\d+)"""
  ]
  DupFields = [ "src_email_address->email_address" ]
  ParserVersion = v1.0.0


}
```