#### Parser Content
```Java
{
Name = mimecast-seg-json-alert-trigger-success-policy
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  ExtractionType = json
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ """"id":""", """"messageInfo":"""", """"status":"""", """"released":""", """"fromHdr":""", """"detectionLevel":""""]
  Fields = [
    """exa_json_path=$.released,exa_field_name=time"""
    """exa_json_path=$.status,exa_field_name=alert_status"""
    """exa_json_path=$.heldReason,exa_field_name=alert_reason"""
    """exa_json_path=$.fromHdr.emailAddress,exa_field_name=src_email_address"""
    """exa_json_path=$.to..emailAddress,exa_field_name=dest_email_address"""
    """exa_json_path=$.subject,exa_field_name=email_subject"""
    """exa_json_path=$.policy,exa_field_name=alert_name"""
    """exa_json_path=$.route,exa_field_name=direction"""
    """exa_json_path=$.detectionLevel,exa_field_name=alert_severity"""
  ]
  DupFields = ["alert_name->alert_type"]


}
```