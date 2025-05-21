#### Parser Content
```Java
{
Name = "rightcrowd-rc-cef-physical-location-access-fail-programmed"
Conditions = [
"""CEF:"""
"""|RightCrowd|RightCrowd|"""
"""|Card not programmed|"""
"""eventId="""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```