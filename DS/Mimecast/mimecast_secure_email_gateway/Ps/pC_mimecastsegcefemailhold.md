#### Parser Content
```Java
{
Name = mimecast-seg-cef-email-hold
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
"""destinationServiceName =Mimecast Email Security"""
""""recipientAddress":""""
""""senderAddress":"""" 
]
  Fields = [
    """"date":"({time}\d+-\d+-\d+T\d+:\d+:\d+\+\d+)""",
    """dproc=({dproc}[^=]+?)\s+\w+=""",
    """"senderIpAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"(?i)Route":"({direction}[^"]+)""",
    """"(?:id|aCode)":"({alert_id}[^"]+)""",
    """"(recipientAddress|Recipient)":"({dest_email_address}[^"]+)""",
    """(senderAddress|Sender)":"(<>|({sender}[^@"]+@[^"]+))""",
    """"(?i)Subject":"({email_subject}[^"]+?)\s*"""",
    """"(messageId|MsgId)":"({message_id}[^"]+)""",
    """"fileName":"({email_attachment}[^"]+\.({file_ext}[^"]+))""",
    """"fileType":"({file_type}[^"]+)""",
    """"fileHash":"({hash_md5}[^"]+)""",
    """"(?:action|actions)":"({action}[^"]+)""",
    """"actionTriggered":"(none|({action}[^"]+))""",
    """"acc":"({user}[^"]+)""",
    """"SourceIP":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"result":"({result}[^"]+)""",
    """"subject":"({email_subject}[^"]+)"""
    """"UrlCategory":"({category}[^"]+)"""
  ]
  DupFields = [ "email_attachment->file_name" ]


}
```