#### Parser Content
```Java
{
Name = checkpoint-avanan-json-email-receive-entitypayload
  Vendor = Check Point
  Product = Check Point Avanan
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json
  Conditions = [ """"entityInfo":""", """"entityPayload":""", """"fromEmail":""", """"isIncoming":true""" ]
  Fields = [
    """exa_json_path=$.entityPayload.received,exa_field_name=time""",
    """exa_json_path=$.entityPayload.fromEmail,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
    """exa_json_path=$.entityPayload.subject,exa_field_name=email_subject""",
    """exa_json_path=$.entityPayload.isQuarantined,exa_field_name=result""",
    """exa_json_path=$.entityPayload.senderClientIp,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))$""",
    """exa_json_path=$.entityPayload.senderServerIp,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))$""",
    """exa_json_path=$.entityPayload.recipients,exa_regex=^\[?({email_recipients}"?({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"?.*?)\s*\]?$""",
    """exa_json_path=$.entityPayload.emailLinks,exa_field_name=additional_info""",
    """exa_json_path=$.entityPayload.attachments,exa_field_name=email_attachments""",
    """exa_json_path=$.entityPayload.internetMessageId,exa_field_name=message_id""",
    """exa_json_path=$.entityPayload.cc,exa_field_name=cc""",
    """exa_json_path=$.entityPayload.bcc,exa_field_name=bcc""",    
    """exa_json_path=$.entityPayload.size,exa_field_name=bytes""",
    """exa_json_path=$.entitySecurityResult.combinedVerdict,exa_field_name=incident_status""",
    """exa_regex=({direction}Incoming)"""
    ]
    ParserVersion = v1.0.0    


}
```