#### Parser Content
```Java
{
Name = forcepoint-ngfw-cef-network-traffic-1004
Conditions = [
  """CEF:"""
  """|FORCEPOINT|Firewall|"""
  """|1004|FW_Related-Connection|"""
]
ParserVersion = "v1.0.0"

moveit-activity.Fields}[
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({file_name}[^.,]+\.({file_ext}[^,]+))"""
    """\sFolderPath:\s*({file_dir}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
  
}
```