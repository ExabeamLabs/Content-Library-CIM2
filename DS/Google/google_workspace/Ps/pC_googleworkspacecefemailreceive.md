#### Parser Content
```Java
{
Name = google-workspace-cef-email-receive
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Google Workspace
  TimeFormat = "epoch"
  Conditions = [ 
"""destinationServiceName =Google Apps""" 
""""service":"smtp-inbound""""
"""dproc=Gmail""" 
]
  Fields = [
    """"timestamp_usec":({time}\d{13})""",
    """"subject":"({email_subject}[^"]+)"""",
    """"destination":\[\{"address[":]*({dest_email_address}[^",]+)"""",
    """"source":\{"address[":]*({src_email_address}[^",]+)""",
    """"service":"({action}[^",]+)""",
    """"success":({result}true|false)""",
    """"rfc2822_message_id"+:"+({message_id}[^",]+)""",
    """"payload_size":({bytes}\d+)""",
    """"client_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\sdestinationServiceName =({app}[^=]+?)\s*\w+="""
  ]
  DupFields = [ "src_email_address->external_address" ]


}
```