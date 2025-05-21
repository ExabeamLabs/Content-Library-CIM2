#### Parser Content
```Java
{
Name = sftp-s-csv-file-delete-success-filedeleted
Conditions = [
  """ sftp-"""
  """"File Deleted""""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```