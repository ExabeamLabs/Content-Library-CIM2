#### Parser Content
```Java
{
Name = sentinelone-singularityp-mix-process-close-processexit
  ParserVersion = v1.0.0
  Product = Singularity Platform
  Conditions = [ """dproc=Deep Visibility Endpoint""", """destinationServiceName =SentinelOne""", """processExit {""" ]
  Fields = ${DLSentinelOneParsersTemplates.sentinelone-activity.Fields} [
    """({event_name}processExit)""",
    """parent.*?path:\s*\\?"+\s*({parent_process}({parent_process_dir}[^@]+?)[\\\/]*({parent_process_name}[^"\\\/]+))\\*".*commandLine:\s*\\?"+\s*({parent_process_command_line}.+?)"\\n?""",
    """\sparent[^\}]+?value:\s"*({parent_process_guid}[^"]+)"""
  ]
  DupFields = ["dest_host->host"]

sentinelone-activity {
    Vendor = SentinelOne
    Product = Singularity
    TimeFormat = "epoch"
    Fields = [
      """\smillisecondsSinceEpoch:\s*({time}\d+)""",
      """\\ncomputer_name:\s*"+({host}[^"]+)""",
      """\\nos_name:\s*"+({os}[^"]+)""",
      """\\nagent_version:\s*"+({user_agent}[^"]+)""",
      """\ssizeBytes:\s*({bytes}\d+)""",
      """user\s*\{[^\}]+?sid:[^"]*?"+({user_sid}[^"\\]+)""",
      """user\s*\{\\n\s+name:\s+[\\\/]?"*((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^\\"]+))""",
      """"app-username":"((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^"]+?))\s*"""",
      """\ssha256:\s*[\\\/]?"+({hash_sha256}[^"\\]+)""",
      """\smd5:\s*[\\\/]?"+({hash_md5}[^"\\]+)""",
      """\spid:\s*({process_id}\d+)""",
      """path:\s+[\\\/]?"+({process_path}({process_dir}[^"]+?)[\\\/]*({process_name}[^"\\\/]+))[\\\/]*"""",
      """destinationAddress\s.*?address:\s*[\\\/]?"+({dest_ip}[^\\"]+)""",
      """destinationAddress\s.*?port:\s*({dest_port}\d+)""",
      """\sstatus:\s*({result}\w+)""",
      """sourceAddress\s.*?port:\s*({src_port}\d+)""",
      """sourceAddress\s.*?address:\s*[\\\/]?"+({src_ip}[^"\\]+)""",
      """sha1:\s*"*({hash_sha1}[^"]+)""""
    
}
```