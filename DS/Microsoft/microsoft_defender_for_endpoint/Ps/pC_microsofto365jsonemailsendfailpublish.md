#### Parser Content
```Java
{
Name = "microsoft-o365-json-email-send-fail-publish"
Vendor = "Microsoft"
Product = "Microsoft Defender for Endpoint"
TimeFormat = "yyyy-MM-dd'T'HH:mm:SSZ"
Conditions = [
  """"category": "AdvancedHunting-EmailEvents""""
  """"operationName": "Publish""""
  """"EmailDirection":"""
]
Fields = [
  """"Timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
  """"RecipientEmailAddress":\s*"({dest_email_address}[^"@\s]+@[^"@\s]+?)""""
  """"SenderFromAddress":\s*"({email_address}[^"@\s]+@[^"@\s]+?)""""
  """"SenderMailFromAddress":\s*"({email_address}[^"@\s]+@[^"@\s]+?)""""
  """"SenderFromDomain":\s*"({email_domain}[^"]+?)""""
  """"EmailDirection":\s*"((?i)unknown|({direction}[^"]+?))""""
  """"Subject":\s*"({email_subject}[^\n]+?)"(,\s*"\w+":|\s*\})"""
  """"SenderIPv4":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"AttachmentCount":\s*({num_attachments}\d+)"""
  """"NetworkMessageId":\s*"({message_id}[^"]+?)""""
  """"DeliveryAction":\s*"({result}[^"]+?)""""
  """({file_verdict}Malicious Payload)"""
]
ParserVersion = "v1.0.0"


}
```