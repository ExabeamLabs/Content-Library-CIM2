#### Parser Content
```Java
{
Name = zeek-z-json-endpoint-login-success-clientaddr
  ParserVersion = v1.0.0
  Product = Zeek
  Conditions = [ """client_addr":""", """"duration":""", """"msg_types":"""]
  Fields = ${ZeekParsersTemplates.json-bro-activity.Fields}[
    """"host_name":"({host}[\w.-]+)""",
    """"client_addr":"({assigned_ip}\d+.\d+.\d+.\d+)""",
    """"domain":"({domain}[^"]+)""",
    """"duration":({duration}[^\}]+)"""
  ]

json-bro-activity = {
  Vendor = Zeek
  Product = zeek
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """"ts\\?"+:[\[\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid\\?"+:\\?"+({connection_id}[^"]+)""",
    """"id\.orig_h\\?"+:\\?"+({src_ip}[a-fA-F\d.:]+)""",
    """"id\.orig_p\\?"+:({src_port}\d+)""",
    """"id\.resp_h\\?"+:\\?"+({dest_ip}[a-fA-F\d.:]+)""",
    """"id\.resp_p\\?"+:({dest_port}\d+)""",
    """"proto\\?"+:\\?"+({protocol}[^"]+)"""
  
}
```