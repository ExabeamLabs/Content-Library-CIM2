#### Parser Content
```Java
{
Name = sentinelone-singularity-cef-file-write-success-dproc
  ParserVersion = v1.0.0
  Conditions = [
    """dproc=Deep Visibility Endpoint"""
    """destinationServiceName =SentinelOne"""
    """fileModification {"""
   ]
  Fields = ${SentinelOneParsersTemplates.sentinelone-activity.Fields} [
    """({event_name}fileModification)""",
    """type"+:"+file"+,"+name"+:"+({file_path}({file_dir}[^"]+?)[\\\/]*({file_name}[^\\\/"]+?(\.({file_ext}[^\.\s"\\\/]+))?))"""",
  ]
  DupFields = ["host->dest_host"]

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