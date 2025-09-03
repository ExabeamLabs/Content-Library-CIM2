#### Parser Content
```Java
{
Name = "abnormalsecurity-as-json-alert-trigger-success-attacktype-1"
ExtractionType = json
ParserVersion = "v1.0.0"
Vendor = "Abnormal Security"
Product = "Abnormal Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [""""abxMessageId":""",""""abxPortalUrl":""",""""attackType":"""",""""attackedParty":"""]
Fields = [
"""exa_json_path=$..receivedTime,exa_field_name=time"""
"""exa_json_path=$..threatId,exa_field_name=alert_id"""
"""exa_json_path=$..subject,exa_field_name=email_subject"""
"""exa_json_path=$..fromAddress,exa_regex=^(|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))$"""
"""exa_json_path=$..toAddresses,exa_regex=^(|({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\"]*))$"""
"""exa_json_path=$..internetMessageId,exa_regex=<*({message_id}[^>\"]+)>*"""
"""exa_json_path=$..autoRemediated,exa_regex=({result}true)"""
"""exa_json_path=$..abxPortalUrl,exa_field_name=additional_info"""
"""exa_json_path=$..attackType,exa_field_name=event_name"""
"""exa_json_path=$..recipientAddress,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""exa_json_path=$..urls[0],exa_field_name=url"""
"""exa_json_path=$..attachmentNames,exa_regex=^\s*\[({email_attachments}"({email_attachment}[^"]+?)"[^\]]*?)\]$"""
]


}
```