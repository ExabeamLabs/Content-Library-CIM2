#### Parser Content
```Java
{
Name = "rightcrowd-rc-cef-physical-location-access-success-validcard"
Conditions = [
"""CEF:"""
"""|RightCrowd|RightCrowd|"""
"""|Valid card|"""
"""eventId="""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```