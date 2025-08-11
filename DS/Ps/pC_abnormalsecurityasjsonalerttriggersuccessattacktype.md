#### Parser Content
```Java
{
Name = "abnormalsecurity-as-json-alert-trigger-success-attacktype"
Conditions = [
""""abx_message_id":"""
  """"abx_portal_url":"""
  """"attack_type":"""
  """"attacked_party":"""
]
ParserVersion = "v1.0.0"

moveit-activity.Fields}[
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({file_name}[^.,]+\.({file_ext}[^,]+))"""
    """\sFolderPath:\s*({file_dir}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
  
}
```