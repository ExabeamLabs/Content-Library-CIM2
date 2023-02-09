#### Parser Content
```Java
{
Name = tanium-im-json-network-traffic-success-networkaccept
  Conditions = [ """"event":"network_accept"""",""""remote_ip"""",""""tanium_computer_id":"""" ]
  Fields = ${TaniumParserTemplates.tanium-operations-1.Fields}[
    """"local_port":({src_port}\d+)""",
    """"remote_port":({dest_port}\d+)""",
    """"local_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"remote_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  ]
  ParserVersion = "v1.0.0"

tanium-operations-1 = {
  Vendor = Tanium
  Product = Tanium Integrity Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
	""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d[+-]\d\d:\d\d)"""",
	""""hostname":"({host}[\w\-.]+)"""",
	""""login__user_name":"({user}[^"]+)"""",
  """"process__login__user_name":"({user}[^"]+)"""",
	""""event":"({event_name}[^"]+)"""",
	""""file__md5":"({hash_md5}[^"]+)"""",
	""""parent_pid":({process_id}\d+)""",
	""""command_line":"({process_command_line}[^"]+?)\s*"""",
	""""parent__command_line":"({parent_process_command_line}[^"]+)\s*"""",
	""""parent_pid":({parent_process_id}\d+)""",
  
}
```