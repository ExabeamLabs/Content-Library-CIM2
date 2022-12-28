#### Parser Content
```Java
{
Name = google-workspace-cef-email-send
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Google Workspace
  TimeFormat = "epoch"
  Conditions = [ 
"""destinationServiceName =Google Apps""" 
"""act=send""" 
"""dproc=Gmail""" 
]
  Fields = [
     """"timestamp_usec":({time}\d{13})""",
     """"destination":\[\{"address[":]*({dest_email_address}[^",]+)"""",
     """"source":\{"address[":]*({email_address}[^",]+)""",
     """"subject":"({email_subject}[^",]+)"""",
     """"selector":"({action}[^",]+)""",
     """"success":({result}true|false)""",
     """"rfc2822_message_id":"({message_id}[^",]+)"""",
     """"payload_size":({bytes}\d+)""",
     """"client_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
     """\sdestinationServiceName =({app}[^=]+?)\s+\w+=""",
     """num_message_attachments":({num_attachments}\d+)"""
  ]
  DupFields = ["dest_email_address->external_address"]


}
```