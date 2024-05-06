#### Parser Content
```Java
{
Name = tanium-cp-json-app-activity-success-tracemoduleserversettings
 ParserVersion = "v1.0.0"
 Product = "Tanium Core Platform"
 Conditions = [ """"table":"TraceModuleServerSettings"""" ]

tanium-template-1 {
    Vendor= Tanium
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ExtractionType = json
    Fields=[
      """"createdAt":"({time}[^"]+)"""",
      """"type":"({alert_type}[^"]+)"""",
      """"connId":"({connection_id}[^"]+)"""",
      """"directoryPath":"({process_dir}[^"]+)"""",
      """"userName":"({user}[\w\.\-]{1,40}\$?)"""",
      """"action":"({action}[^"]+)"""",
      """"dst":"(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))|({dest_host}[^"]+))"""",
# ids is removed
      """"path":"({file_path}({file_dir}.*?)({file_name}[^\\\/;"]+?(\.({file_ext}[^\.;\\"]+?))?))"""",
      """"name":"({alert_name}[^"]+)"""",
# dest_type is removed
      """"query":"({query}.+?)",""",
      """"userId":({user_id}\d+)""",
      """"revision":(null|({revision}\d+))""",
# is_delta is removed
# is_sync is removed
# intel_mapping is removed
      """exa_json_path=$.createdAt,exa_field_name=time"""
      """exa_json_path=$..type,exa_field_name=alert_type"""
      """exa_regex="connId":"({connection_id}[^"]+)"""",
      """exa_regex="directoryPath":"({process_dir}[^"]+)"""",
      """exa_json_path=$.userName,exa_field_name=user"""
      """exa_json_path=$.action,exa_field_name=action"""
      """exa_regex="dst":"(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))|({dest_host}[^"]+))"""",
      """exa_regex="path":"({file_path}({file_dir}.*?)({file_name}[^\\\/;"]+?(\.({file_ext}[^\.;\\"]+?))?))"""",
      """exa_json_path=$..name,exa_field_name=alert_name"""
      """exa_json_path=$..query,exa_field_name=query"""
      """exa_json_path=$.userId,exa_field_name=user_id"""
      """exa_json_path=$.revision,exa_field_name=revision,exa_match_expr=!InList($.revision,"null")"""
    
}
```