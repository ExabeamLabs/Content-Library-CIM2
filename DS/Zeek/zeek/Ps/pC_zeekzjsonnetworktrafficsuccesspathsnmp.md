#### Parser Content
```Java
{
Name = zeek-z-json-network-traffic-success-pathsnmp
  ParserVersion = v1.0.0
  Product = Zeek
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"_path":"snmp""",""""id.orig_h":"""",""""uid":"""",""""id.resp_p":""" ]
  Fields = ${ZeekParsersTemplates.json-zeek-activity.Fields}[
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
  ]

json-zeek-activity = {
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch"
  Fields = [
    """"_system_name":"({host}[\w\-.]+)"""",
    """"ts"+:({time}\d+)""",
    """"uid\\?"+:\\?"+({connection_id}[^"\\]+)""",
    """"id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"id\.orig_p\\?"+:({src_port}\d+)""",
    """"id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"id\.resp_p\\?"+:({dest_port}\d+)""",
  
}
```