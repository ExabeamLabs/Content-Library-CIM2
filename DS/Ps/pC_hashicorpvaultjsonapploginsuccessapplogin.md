#### Parser Content
```Java
{
Name = "hashicorp-vault-json-app-login-success-applogin"
Conditions = [
""""type":"""
""""auth":{"""
""""operation":""""
""""token_type""""
""""source":"/var/log/vault.d/audit.log""""
]
ParserVersion = "v1.0.0"

esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  
}
```