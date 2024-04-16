#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-start-stop-virtcontrol
  ParserVersion = v1.0.0
  Conditions = [ """type=VIRT_CONTROL""", """msg=audit(""", """res=success""", """exe=""" ]

unix-kv-template = {
  Vendor = Unix
  Product = Unix
  TimeFormat = "epoch_sec"
  Fields = [
      """msg=audit\(({time}\d{10})\.\d{3}"""
      """\sauid=({account_id}\d+)\s"""
      """\suid=({user_uid}\d+)"""
      """\sses=({session_id}\d+)""",
      """\spid=({process_id}[^\s]+)\s\w+""",
      """\sres=({result}[^"']+)""",
      """\ssubj=({additional_info}[^=]+)\s+\w+\\?=""",
      """\sacct="({account_name}[^"]+)"""",
      """\sexe="({process_path}({process_dir}[^"]+?)\/[^"\\\/]+)""""
      """\scomm="({process_name}[^\\"]+)"""",
      """\sa0="({process_name}[^"]+)"""",
      """\ssaddr=({src_port}\d+)""",
      """op=({operation}[^\s]+)"""
    ]
 }

}

DLWazuhParserTemplates = {
 wazuh-ssh-login = {
    Vendor = Unix
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"predecoder.hostname":"({host}[^"]+)"""
      """\s({dest_ip}\d+\.\d+\.\d+\.\d+)|({dest_host}[\w\.-]+)\s+sshd\[""",
      """\s({host}[\w\.-]+)\s+sshd\[""",
      """sshd\[({login_id}\d+)""",
      """({event_code}ssh)""",
      """\s+port\s+({src_port}\d+)""",
      """"@timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
      """"data.dstuser":"(\(no user\)|({dest_user}[^"]+))"""
      """"location":"({log_location}[^"]+)"""
      """"path":"({log_path}[^"]+)"""
      """"agent.id":"({agent_id}\d+)"""
      """"manager.name":"({wazuh_manager}[^"]+)"""
      """"rule.description":"({description}[^"]+)"""
      """"decoder.name":"({decoder_name}[^"]+)"""
      """"rule.id":"({rule_id}\d+)"""
      """"agent.name":"({agent_name}[^"]+)"""
      """"agent.id":"({agent_id}[^"]+)"""
      """"data.srcip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    ]
    DupFields = ["dest_host->original_dest_host", "dest_user->user", "decoder_name->process_name"
}
```