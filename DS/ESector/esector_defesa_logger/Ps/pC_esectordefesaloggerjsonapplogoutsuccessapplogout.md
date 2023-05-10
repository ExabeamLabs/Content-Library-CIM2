#### Parser Content
```Java
{
Name = esector-defesalogger-json-app-logout-success-applogout
  ParserVersion = v1.0.0
  Product = ESector DEFESA Logger
  Conditions = [ """"pri":"user""", """"ident":"""", """"ログオフ""", """"receivedFrom":""""]
  Fields = ${ESectorDLParserTemplates.esector-app-log.Fields}[
    """({event_name}ログオフ)"""
  ]

esector-app-log {
    Vendor = ESector
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