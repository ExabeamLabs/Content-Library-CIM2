#### Parser Content
```Java
{
Name = zeek-z-json-ssh-endpoint-ssh
  Vendor = "Zeek"
  Product = "Zeek"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
  """"id.orig_h":"""
  """"id.resp_h":"""
  """"ssh","""
  ]
  Fields = [
    """exa_json_path=$.ts,exa_field_name=time""",
    """exa_json_path=$.uid,exa_field_name=connection_id""",
    """exa_regex="id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex="id\.orig_p\\?"+:({src_port}\d+)""",
    """exa_regex="id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_regex="id\.resp_p\\?"+:({dest_port}\d+)""",
    """exa_json_path=$.direction,exa_field_name=direction""",
    """exa_json_path=$.client,exa_field_name=client"""
    """exa_json_path=$.server,exa_field_name=server""",
    """exa_json_path=$.auth_success,exa_field_name=result"""
   ]
   ParserVersion = "v1.0.0"
},  

${ZeekParsersTemplates.json-bro-activity}{
  Name = zeek-z-json-endpoint-login-success-clientaddr
  ParserVersion = v1.0.0
  Product = Zeek
  Conditions = [ """client_addr":""", """"duration":""", """"msg_types":"""]
  Fields = ${ZeekParsersTemplates.json-bro-activity.Fields}[
    """"host_name":"({host}[\w.-]+)""",
    """"client_addr":"({assigned_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"domain":"({domain}[^"]+)""",
    """"duration":({duration}[^\}]+)"""
  ]


}
```