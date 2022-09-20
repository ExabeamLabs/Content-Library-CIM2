#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-endpoint-login-userlogin
  Vendor = CrowdStrike
  Product = Falcon
  Conditions = [ """"event_simpleName\":\"UserLogon\"""", """"@timestamp"""" ]
  Fields = ${CrowdStrikeParsersTemplates.crowdstrike-auth-activity.Fields} [
    """"LogonType\\*"+:\\*"+({login_type}\d+)""",
    """"LogonDomain\\*"+:\\*"+({domain}[^"\\]+)""",
    """"ClientComputerName\\*"+:\\*"+(-|({dest_host}[^"\\,]+))"""
  ]
  ParserVersion = "v1.0.0"

crowdstrike-auth-activity = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"@timestamp\\*"+:\s*\\*"+({time}[^"\\]\d{10})""",
    """"name\\*"+:\\*"+({event_code}[^"\\]+)""",
    """"event_simpleName\\*"+:\\*"+({event_name}[^"\\]+)""",
    """"event_platform\\*"+:\\*"+({os}[^"\\]+)""",
    """"aip\\*"+:\\*"+({src_ip}[^"\\]+)""",
    """"UserSid\\*"+:\\*"+({user_sid}[^"\\]+)""",
    """"SessionId\\*"+:\\*"+({session_id}[^"\\]+)""",
    """"MD5HashData\\*"+:\\*"+({hash_md5}[^"\\]+)""",
    """"SHA256HashData\\*"+:\\*"+({hash_sha256}[^"\\]+)""",
    """"CommandLine\\*"+:\\*"+\s*({process_command_line}.+?)\s*["\\]""",
    """"TargetProcessId\\*"+:\\*"+({process_id}[^"\\]+)""",
    """"(ImageFileName|TargetFileName)\\*"+:\\*"+(({src_file_path}[^"]+?))\\*"""",
    """"(ImageFileName|TargetFileName)\\*"+:\\*"+({file_dir}[^"]*[\\\/]+)({src_file_name}[^\\\/"]+\.({src_file_ext}[^\\\/"]+))""",
    """"ConfigStateHash\\*"+:\\*"+({old_hash}[^\\"]+)""",
    """"ContextProcessId\\*"+:\\*"+({process_guid}[^\\"]+)""",
    """"Size\\*"+:\\*"+({bytes}\d+)""",
    """"UserName\\*"+:\\*"+(({full_name}({first_name}[^\s"]+)\s({last_name}[^"\\]+))|({user}[^"\\\s]+))""",
    """"FalconHostLink\\*"+:\s*\\*"+({falcon_host_link}[^"]+)"""
  ]
  DupFields = ["event_code->event_name","falcon_host_link->additional_info", "file_dir->directory", "file_name->process_name"
}
```