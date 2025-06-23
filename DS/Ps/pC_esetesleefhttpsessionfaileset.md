#### Parser Content
```Java
{
Name = "eset-es-leef-http-session-fail-eset"
Conditions = [
  """LEEF:"""
  """|ESET|RemoteAdministrator|"""
  """cat=ESET Filtered Website Event"""
  """actionTaken=Blocked"""
]
ParserVersion = "v1.0.0"

moveit-activity.Fields}[
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({file_name}[^.,]+\.({file_ext}[^,]+))"""
    """\sFolderPath:\s*({file_path}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
  
}
```