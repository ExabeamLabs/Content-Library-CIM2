#### Parser Content
```Java
{
Name = tanium-cp-json-app-activity-success-traceconnections
 ParserVersion = "v1.0.0"
 Product = "Tanium Core Platform"
 Conditions = [ """"table":"TraceConnections"""" ]

tanium-template-1 {
    Vendor= Tanium
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields=[
      """"createdAt":"({time}[^"]+)"""",
      """"type":"({alert_type}[^"]+)"""",
      """"connId":"({connection_id}[^"]+)"""",
      """"directoryPath":"({process_dir}[^"]+)"""",
      """"userName":"({user}[^"]+)"""",
      """"action":"({action}[^"]+)"""",
      """"dst":"(({dest_ip}[a-fA-F\d.:]+)|({dest_host}[^"]+))"""",
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
    
}
```