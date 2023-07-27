#### Parser Content
```Java
{
Name = tanium-im-json-file-delete-success-filedelete
  Conditions = [ """"event":"file_delete"""",""""tanium_computer_id":"""",""""process__file__full_path":"""" ]
  Fields = ${TaniumParserTemplates.tanium-operations-1.Fields}[
    """"process__file__full_path":"({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+))"""" 
 ]
 ParserVersion = "v1.0.0"

tanium-operations-1 = {
  Vendor = Tanium
  Product = Tanium Integrity Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
	""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d[+-]\d\d:\d\d)"""",
	""""hostname":"({host}[\w\-.]+)"""",
	""""login__user_name":"({user}[\w\.\-]{1,40}\$?)"""",
  """"process__login__user_name":"({user}[\w\.\-]{1,40}\$?)"""",
	""""event":"({event_name}[^"]+)"""",
	""""file__md5":"({hash_md5}[^"]+)"""",
	""""parent_pid":({process_id}\d+)""",
	""""command_line":"({process_command_line}[^"]+?)\s*"""",
	""""parent__command_line":"({parent_process_command_line}[^"]+)\s*"""",
	""""parent_pid":({parent_process_id}\d+)""",
  
}
```