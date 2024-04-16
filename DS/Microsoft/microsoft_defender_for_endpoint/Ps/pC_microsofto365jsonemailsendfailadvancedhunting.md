#### Parser Content
```Java
{
Name = "microsoft-o365-json-email-send-fail-advancedhunting"
ExtractionType = json
Vendor = "Microsoft"
Product = "Microsoft Defender for Endpoint"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
Conditions = [
  """EmailAttachmentInfo""""
  """"FileName":"""
  """"FileType":"""
]
Fields = [
  """"Timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
  """"RecipientEmailAddress":\s*"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"SenderFromAddress":\s*"({email_address}[^"@\s]+@[^"@\s]+?)""""
  """"category":\s*"({category}[^"]+?)""""
  """"FileName":\s*"({file_name}[^"\.]+?(\.({file_ext}[^"]+?))?)""""
  """"FileType":\s*"({file_type}[^"]+?)""""
  """"NetworkMessageId":\s*"({message_id}[^"]+?)""""
  """"FileSize":({bytes}\d+)"""
  """exa_json_path=$.properties.Timestamp,exa_field_name=time"""
  """exa_json_path=$.properties.RecipientEmailAddress,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.properties.SenderFromAddress,exa_field_name=email_address"""
  """exa_json_path=$.category,exa_field_name=category"""
  """exa_json_path=$.properties.FileName,exa_field_name=file_name"""
  """exa_json_path=$.properties.FileType,exa_field_name=file_type"""
  """exa_json_path=$.properties.NetworkMessageId,exa_field_name=message_id"""
  """exa_json_path=$.properties.FileSize,exa_field_name=bytes"""
]
DupFields = [
  "file_name->email_attachment"
]
ParserVersion = "v1.0.0"


}
```