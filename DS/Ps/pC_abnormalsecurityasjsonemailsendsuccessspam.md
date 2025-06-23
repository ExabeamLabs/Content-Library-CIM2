#### Parser Content
```Java
{
Name = "abnormalsecurity-as-json-email-send-success-spam"
Conditions = [
""""abx_message_id":"""
  """"abx_portal_url":"""
  """"attack_type":"""
  """"Spam","""
  """"attacked_party":"""

]
ExtractionType = json
ParserVersion = "v1.0.0"

moveit-activity.Fields}[
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({file_name}[^.,]+\.({file_ext}[^,]+))"""
    """\sFolderPath:\s*({file_path}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
  
}
```