#### Parser Content
```Java
{
Name = mimecast-seg-cef-email-inbound
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
""""aCode":""""
""""acc":""""
""""Route":"In"""
""""MsgId":""""
""""Subject":"""
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ([\w.\-]+) """,
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
    """"(?i)Route":"({direction}[^"]+)""",
    """"(?:id|aCode)":"({alert_id}[^"]+)""",
    """"(recipientAddress|Recipient)":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """(senderAddress|Sender)":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))""",
    """headerFrom":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))""",
    """"SenderDomain":"({email_domain}[^"]+)"""",
    """"(?i)Subject":"({email_subject}[^"]+?)\s*"""",
    """"(messageId|MsgId)":"<({message_id}[^"]+)>"""",
    """"(?:action|actions)":"({action}[^"]+)""",
    """"actionTriggered":"({action}[^"]+)""",
    """"(Source)?IP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"fileName":"({email_attachment}[^"]+)"""",
    """"Size":({bytes}\d+)""",
    """"Virus":"({alert_name}[^"]+)""""
    """"UrlCategory":"({category}[^"]+)"""
  ]
  DupFields = ["dest_email_address->email_user"]


}
```