#### Parser Content
```Java
{
Name = esector-defesalogger-json-file-delete-success-user
  ParserVersion = "v1.0.0"
  Conditions = [ """"pri":"user""", """"ident":"""", """"ファイル削除""", """"receivedFrom":""""]
  Fields = ${ESectorParserTemplates.esector-file-activity.Fields}[
    """ファイル削除\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル削除)"""
  ]

esector-file-activity {
    Vendor = ESector
    Product = ESector DEFESA Logger
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)[+-]\d\d:\d\d\s+\w+""",
      """receivedFrom":"({host}[^"]+)""",
      """host":"({host_ip}[a-fA-F:\.\d]+)"""",
      """ident":"({app}[^"]+)"""",
      """"message":([^,]+,){2}\\"({src_host}[^\\"]+)\\"""",
      """"message":([^,]+,){3}\\"([\w+\\-]+?-)?({user}[^\\"]+)\\""""
    
}
```