#### Parser Content
```Java
{
Name = "microsoft-o365-json-email-send-fail-publish"
ExtractionType = json
Vendor = "Microsoft"
Product = "Microsoft Defender for Endpoint"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
Conditions = [
  """EmailEvents""""
  """"EmailDirection":"""
]
Fields = [
  """"Timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
  """"RecipientEmailAddress":\s*"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"SenderFromDomain":\s*"({src_email_domain}[^"]+?)""""
  """"SenderFromAddress":\s*"({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"SenderMailFromAddress":\s*"({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"EmailDirection":\s*"((?i)unknown|({direction}[^"]+?))""""
  """"Subject":\s*"({email_subject}[^\n]+?)"(,\s*"\w+":|\s*\})"""
  """"SenderIPv4":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"AttachmentCount":\s*({attachment_count}\d+)"""
  """"NetworkMessageId":\s*"({message_id}[^"]+?)""""
  """"DeliveryAction":\s*"({result}[^"]+?)""""
  """({file_verdict}Malicious Payload)"""
  """"operationName":\s*"({operation}[^"]+)""""
  """"category":\s*"({category}[^"]+)""""
  """exa_json_path=$..Timestamp,exa_field_name=time"""
  """exa_json_path=$..RecipientEmailAddress,exa_regex=\s*({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""" 
  """exa_json_path=$..SenderFromDomain,exa_field_name=src_email_domain"""
  """exa_json_path=$..SenderFromAddress,exa_regex=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$..SenderMailFromAddress,exa_regex=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$..EmailDirection,exa_regex=((?i)unknown|({direction}[^"]+))"""
  """exa_json_path=$..Subject,exa_field_name=email_subject"""
  """exa_json_path=$..SenderIPv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$..AttachmentCount,exa_field_name=attachment_count"""
  """exa_json_path=$..NetworkMessageId,exa_field_name=message_id"""
  """exa_json_path=$..DeliveryAction,exa_field_name=result"""
  """exa_json_path=$.operationName,exa_field_name=operation"""
  """exa_json_path=$.category,exa_field_name=category"""
  """exa_regex=({file_verdict}Malicious Payload)"""
]
ParserVersion = "v1.0.0"


}
```