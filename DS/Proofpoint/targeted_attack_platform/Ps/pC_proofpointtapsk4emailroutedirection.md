#### Parser Content
```Java
{
Name = proofpoint-tap-sk4-email-routedirection
Vendor = Proofpoint
Product = Targeted Attack Platform
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """routeDirection"""
  """ProofPointMessageLog_CL"""
]
Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(\.\d+)?(Z)?""""
  """"detectedSizeBytes":\s+({bytes}\d+)""""
  """"detectedSizeBytes":\s+({bytes}\d+),\s+""""
  """"msg_normalizedHeader_from_s":"(\[|\s|\\|")*[^\]]+?<({src_email_address}[^>]+?)>"""
  """"msg_normalizedHeader_from_s":"(\[|\s|\\|")*({src_email_address}[<^,"]+?@[^>]+?)\\""""
  """"envelope_from_s":"({src_email_address}[^"]+)""""
  """"smtp\.mailfrom": "({src_email_address}[^"]+)""""
  """"filter_verified_rcpts_s":"\[\s*\\*"({email_recipients}.+?)\\*"\s*\]","""
  """"filter_verified_rcpts_s":"\[[^"]*"({dest_email_address}[^,]+?@[^,]+?)[\s\\"]+"""
  """"msg_header_subject_s":"\[\s*\\*"({email_subject}[^\]]+?)\\*"\s*\]",""""
  """"filter_routeDirection_s":"({direction}[^"]+)""""
  """"filter_disposition_s":"({result}[^"]+)"""
  """"detectedName":\s*"({email_attachment}(?!text)[^"]+)"""
  """"filter_isMsgReinjected_b":[\s"]*({is_consolidated}\w+)[\s"]*,"""
  """"rule":\s*"({rule}[^"]+)""""
]
DupFields = [
  "email_attachment->email_attachments"
]
ParserVersion = "v1.0.0"


}
```