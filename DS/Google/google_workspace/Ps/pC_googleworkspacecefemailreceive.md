#### Parser Content
```Java
{
Name = google-workspace-cef-email-receive
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Google Workspace
  TimeFormat = "epoch"
  Conditions = [ 
""""source":"""
""""destination":""" 
""""service":"smtp-inbound""""
""""service":"gmail-ui"""" 
]
  Fields = [
    """"timestamp_usec":({time}\d{13})""",
    """"subject":"({email_subject}[^"]+)"""",
    """"destination":\[\{"address[":]*({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"source":\{"address":"({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-\\]+)*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"service":"({action}[^",]+)""",
    """"success":({result}true|false)""",
    """"rfc2822_message_id"+:"+({message_id}[^",]+)""",
    """"payload_size":({bytes}\d+)""",
    """"client_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\sdestinationServiceName =({app}[^=]+?)\s*\w+=""",
    """"attachment":\[[^\}]+"file_name":"({email_attachment}[^\}]+?)"(,|\})""",
    """num_message_attachments":({num_attachments}\d+)"""
  ]
  DupFields = [ "src_email_address->external_address" ]


}
```