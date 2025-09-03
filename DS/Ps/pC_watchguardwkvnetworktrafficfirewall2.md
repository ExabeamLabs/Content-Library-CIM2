#### Parser Content
```Java
{
Name = watchguard-w-kv-network-traffic-firewall-2
Conditions = [
  """msg_id="""
  """3000-0151"""
  """firewall:"""
]
ParserVersion = "v1.0.0"

moveit-activity.Fields}[
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({file_name}[^.,]+\.({file_ext}[^,]+))"""
    """\sFolderPath:\s*({file_dir}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
  
}
```