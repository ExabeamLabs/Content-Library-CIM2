#### Parser Content
```Java
{
Name = esector-defesa-json-app-activity-appactivity
  ParserVersion = v1.0.0
  Product = ESector DEFESA
  Conditions = [ """"pri":"user""", """message""", """"receivedFrom":"""", """"ident":""""]
  Fields = ${ESectorDLParserTemplates.esector-app-log.Fields}[
    """"message":([^,]+,){4}\\"({event_name}[^\\"]+)\\""""
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