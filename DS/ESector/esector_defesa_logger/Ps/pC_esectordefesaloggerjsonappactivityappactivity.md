#### Parser Content
```Java
{
Name = esector-defesalogger-json-app-activity-appactivity
  ParserVersion = v1.0.0
  Product = ESector DEFESA Logger
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
      """host":"({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
      """ident":"({app}[^"]+)"""",
      """"message":([^,]+,){2}\\"({src_host}[^\\"]+)\\"""",
      """"message":([^,]+,){3}\\"([\w+\\-]+?-)?({user}[^\\"]+)\\""""
    
}
```