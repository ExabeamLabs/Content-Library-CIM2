#### Parser Content
```Java
{
Name = mimecast-es-cef-email-hold
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Email Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
"""destinationServiceName =Mimecast Email Security"""
""""recipientAddress":""""
""""senderAddress":"""" 
]
  Fields = [
    """"date":"({time}\d+-\d+-\d+T\d+:\d+:\d+\+\d+)""",
    """dproc=({dproc}[^=]+?)\s+\w+=""",
    """"senderIpAddress":"({src_ip}[\da-fA-F.:]+)"""",
    """"(?i)Route":"({direction}[^"]+)""",
    """"(?:id|aCode)":"({alert_id}[^"]+)""",
    """"(recipientAddress|Recipient)":"({dest_email_address}[^"]+)""",
    """(senderAddress|Sender)":"(<>|({email_address}[^@"]+@[^"]+))""",
    """"(?i)Subject":"({email_subject}[^"]+?)\s*"""",
    """"(messageId|MsgId)":"({message_id}[^"]+)""",
    """"fileName":"({email_attachment}[^"]+\.({file_ext}[^"]+))""",
    """"fileType":"({file_type}[^"]+)""",
    """"fileHash":"({hash_md5}[^"]+)""",
    """"(?:action|actions)":"({action}[^"]+)""",
    """"actionTriggered":"(none|({action}[^"]+))""",
    """"acc":"({user}[^"]+)""",
    """"SourceIP":"({src_ip}[^"]+)"""",
    """"result":"({result}[^"]+)""",
    """"subject":"({email_subject}[^"]+)"""
  ]


}
```