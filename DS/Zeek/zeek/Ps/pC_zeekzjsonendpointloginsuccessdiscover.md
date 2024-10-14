#### Parser Content
```Java
{
Name = "zeek-z-json-endpoint-login-success-discover"
Conditions = [
""" zeek_dhcp """
"""msg_type"""
]
ParserVersion = "v1.0.0"

zeek-ldap-events.Fields}[
    """"_path":"({auth_method}[^"]+)""""
  ]
  ParserVersion = v1.0.0
},

${ZeekParsersTemplates.zeek-ldap-events}{
  Name = zeek-z-json-endpoint-authentication-success-ldapbind
  Conditions = [ """"id.orig_h""", """"id.resp_h""", """"opcode":["""", """"_path":"ldap"""", """["bind"]""" ]
  Fields = ${ZeekParsersTemplates.zeek-ldap-events.Fields}[
    """"_path":"({auth_method}[^"]+)""""
  ]
  ParserVersion = v1.0.0
},

${ZeekParsersTemplates.zeek-ldap-events}{
  Name = zeek-z-json-app-activity-success-ldapunbind
  Conditions = [ """"id.orig_h""", """"id.resp_h""", """"opcode":["""", """"_path":"ldap"""", """["unbind"]""" ]
  Fields = ${ZeekParsersTemplates.zeek-ldap-events.Fields}[
    """"_path":"({app}[^"]+)""""
  ]
  ParserVersion = v1.0.0
},

${ZeekParsersTemplates.zeek-ldap-events}{
  Name = zeek-z-json-app-activity-success-ldapbindsimple
  Conditions = [ """"id.orig_h""", """"id.resp_h""", """"opcode":["""", """"_path":"ldap"""", """["bind simple"]""" ]
  Fields = ${ZeekParsersTemplates.zeek-ldap-events.Fields}[
    """"_path":"({app}[^"]+)""""
  ]
  ParserVersion = v1.0.0
}

]
#=================================================== End of ZeekParsers section =====================================================================

#=================================================== Start of ZeekParsersDL section ==================================================================
ZeekParsersDL = [

{
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "epoch_sec"
Fields = [
""""_system_name":"({host}[\w\-.]+)""""
""""ts"+:({time}\d{10})"""
""""uid\\?"+:\\?"+({connection_id}[^"\\]+)"""
""""id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""id\.orig_p\\?"+:({src_port}\d+)"""
""""id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""id\.resp_p\\?"+:({dest_port}\d+)"""
""""mac"+:"+({src_mac}[^"]+)"""
""""ts"+:({time}\d+)"""
""""uids"+:\["+({user_uids}[^"]+)"""
""""msg_types"+:\["+({dhcp_type}[^"]+)"""
]
Name = "zeek-z-json-endpoint-login-success-discover"
Conditions = [
""" zeek_dhcp """
"""msg_type"""
]
ParserVersion = "v1.0.0"
}

{
  Name = zeek-z-json-endpoint-authentication-ssl
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """"id.orig_h":""", """"id.resp_h":""", """"ssl",""" ]
  Fields = [
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid":"({connection_id}[^"]+)""",
    """"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"id\.orig_p":({src_port}\d+)""",
    """"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"id\.resp_p":({dest_port}\d+)""",
    """"cipher":({auth_method}[^,]+)""",
    """"server_name":"({dest_host}[^"]+)""",
    """"validation_status":"({result}[^"]+)""",
    """"ja3":"({ja3}[^"]+)""",
# issuer is removed
  
}
```