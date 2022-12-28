#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-endpoint-login-fail-userlogonfail
  Vendor = CrowdStrike
  Product = Falcon
  Conditions = [ """"event_simpleName\":\"UserLogonFailed2\"""", """"@timestamp"""" ]
  ParserVersion = "v1.0.0"

crowdstrike-auth-activity = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"@timestamp\\*"+:\s*\\*"+({time}[^"\\]\d{10})""",
    """"name\\*"+:\\*"+({name}[^"\\]+)""",
    """"event_simpleName\\*"+:\\*"+({event_name}[^"\\]+)""",
    """"event_platform\\*"+:\\*"+({os}[^"\\]+)""",
    """"aip\\*"+:\\*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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
    """"UserName\\*"+:\\*"+(({full_name}({first_name}[^\s"]+)\s({last_name}[^"\\]+))|({user}[^"\\\s]+))""",
    """"FalconHostLink\\*"+:\s*\\*"+({falcon_host_link}[^"]+)"""
    """"aid":"({aid}[^"]+)"""
  ]
  DupFields = ["event_name->event_code", "falcon_host_link->additional_info", "file_dir->directory", "file_name->process_name"
}
```