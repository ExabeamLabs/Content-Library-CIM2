#### Parser Content
```Java
{
Name = checkpoint-avanan-json-alert-trigger-success-dlp
  ParserVersion = v1.0.0
  Conditions = [ """type":"avanan_security_event_dlp"""", """"dlp_detections"""", """"security_event"""", """"severity"""" ]

json-avanan-security-alert = {
  Vendor = Check Point
  Product = Check Point Avanan
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"time":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """"(event|source)type\\*":\\*"({alert_name}[^\\"]+)""",
    """"severity\\*":({alert_severity}[^,]+?)\}?,""",
    """"entity_info\\*":\{[^\}]+?"entity_id\\*":\\*"({alert_id}[^"\\]+)""",
    """"entity_info\\*":\{[^\}]+?"entity_sub_type\\*":\\*"({alert_type}[^"\\]+)""",
    """"(entity_)?payload\\*":\{[^\}]+?"subject\\*":\\*"\s*({email_subject}[^"\\]+?)\s*\\*"""",
    """"subject\\*":\\*"\s*({email_subject}[^\\"]+?)\s*\\*"""",
    """"saas_info\\*":\{[^\}]+?"full_name\\*":\\*"({full_name}[^\\"]+)\\*"""",
  //  """"saas_info\\*":\{[^\}]+?"email\\*":\\*"({email_address}[^\\"]+)\\*"""",
    """("entity\\*":\{[^\}]+)?"recipients\\*":\[\\*"*({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\\*"\],""",
    """"description_text\\*":\\*"({additional_info}[^\[]+?)\\*",""",
    """"is_quarantined\\*":({result}[^,]+)""",
    """sender_client_ip\\*":\\*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """attachments\\*":\[\{[^\}]+?"name\\*":\\*"({email_attachments}[^"\\]+)""",
    """file_name\\*":\\*"\s*({file_name}[^\\"]+?)\s*\\*"""",
    """from_email\\*":\\*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"category":"({category}[^"]+)""""
    
}
```