#### Parser Content
```Java
{
Name = accellion-kw-json-email-send-success-sendemail
Conditions = [
  """url_host"""
  """app_host"""
  """description"""
  """send_mail"""
  """event"""
]
ExtractionType = json
DupFields = ["email_recipients->dest_email_address" , "email_address->src_email_address"]
ParserVersion = "v1.0.0"


}
```