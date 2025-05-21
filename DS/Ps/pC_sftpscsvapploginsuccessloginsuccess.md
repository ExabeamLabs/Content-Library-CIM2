#### Parser Content
```Java
{
Name = "sftp-s-csv-app-login-success-loginsuccess"
Conditions = [
""" sftp-"""
""""Login Success""""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```