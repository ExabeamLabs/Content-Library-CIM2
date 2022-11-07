#### Parser Content
```Java
{
Name = esector-defesa-json-file-write-success-user-2
  ParserVersion = "v1.0.0"
  Conditions = [ """"pri":"user""", """"ident":"""", """"ファイルコピー""", """"receivedFrom":""""]
  Fields = ${ESectorParserTemplates.esector-file-activity.Fields}[
    """ファイルコピー\\",\\"({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}[^\\\.]+))?))\\"""",
    """({event_name}ファイルコピー)"""
  ]

esector-file-activity {
    Vendor = ESector
    Product = ESector DEFESA
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)[+-]\d\d:\d\d\s+\w+""",
      """receivedFrom":"({host}[^"]+)""",
      """host":"({host_ip}[a-fA-F:\.\d]+)"""",
      """ident":"({app}[^"]+)"""",
      """"message":([^,]+,){2}"({src_host}[^"]+)"""",
      """"message":([^,]+,){3}"([\w+\\-]+?-)?({user}[^"]+)""""
    
}
```