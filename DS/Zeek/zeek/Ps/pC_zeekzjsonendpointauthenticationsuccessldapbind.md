#### Parser Content
```Java
{
Name = zeek-z-json-endpoint-authentication-success-ldapbind
  Conditions = [ """"id.orig_h""", """"id.resp_h""", """"opcode":["""", """"_path":"ldap"""", """["bind"]""" ]
  Fields = ${ZeekParsersTemplates.zeek-ldap-events.Fields}[
    """"_path":"({auth_method}[^"]+)""""
  ]
  ParserVersion = v1.0.0

zeek-ldap-events = {
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
    """"_system_name":"({host}[^"]+)""",
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)""",
    """"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"id\.orig_p":({src_port}\d+)""",
    """"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"id\.resp_p":({dest_port}\d+)""",
    """"proto":"({protocol}[^"]+)""",
    """"opcode":\["({operation}[^"]+)"""",
    """"uid":"({user_uid}[^"]+)"""",
    """"result":\["({result}[^"]+)""""
  
}
```