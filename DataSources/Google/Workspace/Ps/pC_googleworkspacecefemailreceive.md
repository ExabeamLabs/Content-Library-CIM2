#### Parser Content
```Java
{
Name = google-workspace-cef-email-receive
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Workspace
  TimeFormat = "epoch"
  Conditions = [ 
"""destinationServiceName =Google Apps""" 
""""service":"smtp-inbound""""
"""dproc=Gmail""" 
]
  Fields = [
    """"timestamp_usec":({time}\d+)""",
    """"subject":"({email_subject}[^"]+)"""",
    """"destination":\[\{"address[":]*({dest_email_address}[^",]+)"""",
    """"source":\{"address[":]*({email_address}[^",]+)""",
    """"service":"({action}[^",]+)""",
    """"success":({result}true|false)""",
    """"rfc2822_message_id"+:"+({message_id}[^",]+)""",
    """"payload_size":({bytes}\d+)""",
    """"client_ip":"({src_ip}[a-fA-F\d.:]+)"""",
    """\sdestinationServiceName =({app}[^=]+?)\s*\w+="""
  ]


}
```