#### Parser Content
```Java
{
Name = esector-defesalogger-json-file-write-success-user-1
  ParserVersion = "v1.0.0"
  Conditions = [ """"pri":"user""", """"ident":"""", """"ファイル移動""", """"receivedFrom":""""]
  Fields = ${ESectorParserTemplates.esector-file-activity.Fields}[
    """ファイル移動\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイル移動)"""
  ]

esector-file-activity {
    Vendor = ESector
    Product = ESector DEFESA Logger
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)[+-]\d\d:\d\d\s+\w+""",
      """receivedFrom":"({host}[^"]+)""",
      """host":"({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
      """ident":"({app}[^"]+)"""",
      """"message":([^,]+,){2}\\"({src_host}[^\\"]+)\\"""",
      """"message":([^,]+,){3}\\"([\w+\\-]+?-)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\""""
    
}
```