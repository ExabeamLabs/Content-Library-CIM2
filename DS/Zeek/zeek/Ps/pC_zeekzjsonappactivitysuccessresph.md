#### Parser Content
```Java
{
Name = zeek-z-json-app-activity-success-resph
  Product = Zeek
  ParserVersion = v1.0.0
  Conditions = [ """"id.orig_h""", """"id.resp_h""", """"command":""", """"user""", """"reply_code""" ]
  Fields = ${ZeekParsersTemplates.json-bro-activity.Fields}[
    """"user":\s*"((?i)<unknown>|({user}[\w\.\-]{1,40}\$?))""",
    """"password":\s*"({password}[^"]+)""",
    """"command":\s*"({operation}[^"]+)""",
    """"reply_code":\s*({trans_id}\d+)""",
    """"reply_msg":\s*"({additional_info}[^=]+?)",""",
    """"data_channel\.resp_p":\s*({dest_port}\d+)""",
  ]

json-bro-activity = {
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """"ts\\?"+:[\[\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid\\?"+:\\?"+({connection_id}[^"]+)""",
    """"id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"id\.orig_p\\?"+:({src_port}\d+)""",
    """"id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"id\.resp_p\\?"+:({dest_port}\d+)""",
    """"proto\\?"+:\\?"+({protocol}[^"]+)"""
  
}
```