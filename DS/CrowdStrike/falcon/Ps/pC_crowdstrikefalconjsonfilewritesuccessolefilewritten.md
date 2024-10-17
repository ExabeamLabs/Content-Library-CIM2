#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-file-write-success-olefilewritten
  ParserVersion = v1.0.0  
  Product = Falcon
  Conditions = [ """"event_simpleName\":\"OleFileWritten\"""", """\"aip\"""", """\"aid\"""" ]

crowdstrike-auth-activity = {
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"@?timestamp\\*"+:\s*\\*"+({time}\d{10})""",
    """"name\\*"+:\\*"+({name}[^"\\]+)""",
    """"event_simpleName\\*"+:\\*"+({event_name}[^"\\]+)""",
    """"event_platform\\*"+:\\*"+({os}[^"\\]+)""",
    """"aip\\*"+:\\*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"UserSid\\*"+:\\*"+({user_sid}[^"\\]+)""",
    """"SessionId\\*"+:\\*"+({session_id}[^"\\]+)""",
    """"MD5HashData\\*"+:\\*"+({hash_md5}[^"\\]+)""",
    """"SHA256HashData\\*"+:\\*"+({hash_sha256}[^"\\]+)""",
    """"CommandLine\\*"+:\\*"+\s*({process_command_line}.+?)\s*["\\]""",
    """"TargetProcessId\\*"+:\\*"+({process_id}[^"\\]+)""",
    """"(ImageFileName|TargetFileName)\\*"+:\\*"+(({file_path}[^"]+?))\\*"""",
    """"(ImageFileName|TargetFileName)\\*"+:\\*"+({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))""",
    """"ConfigStateHash\\*"+:\\*"+({old_hash}[^\\"]+)""",
    """"ContextProcessId\\*"+:\\*"+({process_guid}[^\\"]+)""",
    """"Size\\*"+:\\*"+({bytes}\d+)""",
    """"UserName\\*"+:\\*"+((?i)system|({full_name}({first_name}[^\s"]+)\s({last_name}[^"\\]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"FalconHostLink\\*"+:\s*\\*"+({falcon_host_link}[^"]+)"""
    """"aid\\?":\\?"({aid}[^"]+?)\\?""""
    """"event_platform\\?":\\?"({os}[^"]+?)\\?""""
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.message,exa_regex="name\\*"+:\\*"+({name}[^"\\]+)""",
    """exa_json_path=$.message,exa_regex=event_simpleName\\*"+:\\*"+({event_name}[^"\\]+)""",
    """exa_json_path=$.message,exa_regex=event_platform\\*"+:\\*"+({os}[^"\\]+)""",
    """exa_json_path=$.message,exa_regex=aip\\*"+:\\*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.message,exa_regex=UserSid\\*"+:\\*"+({user_sid}[^"\\]+)""",
    """exa_json_path=$.message,exa_regex=SessionId\\*"+:\\*"+({session_id}[^"\\]+)""",
    """exa_json_path=$.message,exa_regex=MD5HashData\\*"+:\\*"+({hash_md5}[^"\\]+)""",
    """exa_json_path=$.message,exa_regex=SHA256HashData\\*"+:\\*"+({hash_sha256}[^"\\]+)""",
    """exa_json_path=$.message,exa_regex=CommandLine\\*"+:\\*"+\s*({process_command_line}.+?)\s*["\\]""",
    """exa_json_path=$.message,exa_regex=TargetProcessId\\*"+:\\*"+({process_id}[^"\\]+)""",
    """exa_json_path=$.message,exa_regex="(ImageFileName|TargetFileName)\\*"+:\\*"+(({file_path}[^"]+?))\\*"""",
    """exa_json_path=$.message,exa_regex="(ImageFileName|TargetFileName)\\*"+:\\*"+({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))""",
    """exa_json_path=$.message,exa_regex="ConfigStateHash\\*"+:\\*"+({old_hash}[^\\"]+)""",
    """exa_json_path=$.message,exa_regex="ContextProcessId\\*"+:\\*"+({process_guid}[^\\"]+)""",
    """exa_json_path=$.message,exa_regex="Size\\*"+:\\*"+({bytes}\d+)""",
    """exa_json_path=$.message,exa_regex="UserName\\*"+:\\*"+((?i)system|({full_name}({first_name}[^\s"]+)\s({last_name}[^"\\]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.message,exa_regex="FalconHostLink\\*"+:\s*\\*"+({falcon_host_link}[^"]+)"""
    """exa_json_path=$.message,exa_regex="aid\\?":\\?"({aid}[^"]+?)\\?""""
    """exa_json_path=$.message,exa_regex="event_platform\\?":\\?"({os}[^"]+?)\\?""""
  ]
  DupFields = ["event_name->event_code", "falcon_host_link->additional_info", "file_dir->directory", "file_name->process_name"
}
```