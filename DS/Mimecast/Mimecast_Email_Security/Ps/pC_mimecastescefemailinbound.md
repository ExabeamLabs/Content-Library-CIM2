#### Parser Content
```Java
{
Name = mimecast-es-cef-email-inbound
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Email Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
"""destinationServiceName =Mimecast Email Security"""
""""acc":""""
""""Route":""""
""""MsgId":""""
""""Subject":""""
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ([\w.\-]+) """,
    """"(?i)Route":"({direction}[^"]+)""",
    """"(?:id|aCode)":"({alert_id}[^"]+)""",
    """"(recipientAddress|Recipient)":"({dest_email_address}[^"]+)""",
    """(senderAddress|Sender)":"(<>|({email_address}[^"]+))""",
    """"(?i)Subject":"({email_subject}[^"]+?)\s*"""",
    """"(messageId|MsgId)":"({message_id}[^"]+)""",
    """"(?:action|actions)":"({action}[^"]+)""",
    """"actionTriggered":"({action}[^"]+)""",
    """"acc":"({user}[^"]+)""",
    """"(Source)?IP":"({src_ip}[^"]+)"""",
    """"fileName":"({email_attachment}[^"]+)"""",
    """"Size":({bytes}\d+)""",
    """"Virus":"({alert_name}[^"]+)""""
  ]


}
```