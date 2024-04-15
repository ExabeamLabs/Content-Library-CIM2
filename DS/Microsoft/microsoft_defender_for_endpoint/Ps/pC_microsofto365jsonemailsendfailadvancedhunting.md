#### Parser Content
```Java
{
Name = "microsoft-o365-json-email-send-fail-advancedhunting"
Vendor = "Microsoft"
Product = "Microsoft Defender for Endpoint"
TimeFormat = "yyyy-MM-dd'T'HH:mm:SSZ"
Conditions = [
  """"category": "AdvancedHunting-EmailAttachmentInfo""""
  """"operationName": "Publish""""
  """"FileName":"""
  """"FileType":"""
]
Fields = [
  """"Timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
  """"RecipientEmailAddress":\s*"({dest_email_address}[^"@\s]+@[^"@\s]+?)""""
  """"SenderFromAddress":\s*"({email_address}[^"@\s]+@[^"@\s]+?)""""
  """"category":\s*"({category}[^"]+?)""""
  """"FileName":\s*"({file_name}[^"\.]+?(\.({file_ext}[^"]+?))?)""""
  """"FileType":\s*"({file_type}[^"]+?)""""
  """"NetworkMessageId":\s*"({message_id}[^"]+?)""""
]
DupFields = [
  "file_name->email_attachment"
]
ParserVersion = "v1.0.0"


}
```