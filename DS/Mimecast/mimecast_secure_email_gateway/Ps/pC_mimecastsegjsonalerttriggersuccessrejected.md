#### Parser Content
```Java
{
Name = mimecast-seg-json-alert-trigger-success-rejected
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  ExtractionType = json
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ """"fromAddress":""", """"toAddress":"""", """"description":"""", """"created":""", """"ipAddress":""", """"manageRecipient":"""]
  Fields = [
    """exa_json_path=$.fromAddress,exa_field_name=email_address"""
    """exa_json_path=$.toAddress,exa_field_name=dest_email_address"""
    """exa_json_path=$.description,exa_field_name=additional_info"""
    """exa_json_path=$.created,exa_field_name=time"""
    """exa_json_path=$.ipAddress,exa_field_name=src_ip"""
    """exa_json_path=$.id,exa_field_name=message_id"""
    """exa_json_path=$.spamScore,exa_field_name=spam_score"""
    """exa_json_path=$.description,exa_field_name=alert_reason"""
  ]


}
```