#### Parser Content
```Java
{
Name = sentinelone-singularityp-sk4-registry-modify-regvaluemodified
  ParserVersion = "v1.0.0"
  Product = Singularity Platform
  Conditions = [ """dproc=Deep Visibility Endpoint""", """destinationServiceName =SentinelOne""", """regValueModified {""" ]
  Fields = ${DLSentinelOneParsersTemplates.sentinelone-activity.Fields} [
    """({event_name}regValueModified)""",
  ]

sentinelone-activity {
    Vendor = SentinelOne
    Product = Singularity Platform
    TimeFormat = "epoch"
    Conditions = [
    """dproc=Deep Visibility Endpoint""",
    """destinationServiceName =SentinelOne""",
    """method:""",
    """http {"""
    ]
    Fields = [
      """\smillisecondsSinceEpoch:\s*({time}\d{13})""",
      """\\ncomputer_name:\s*"+({host}[\w\-.]+)"""",
      """\\ncomputer_name:\s*"+({dest_translated_host}[^"]+)"""",
      """\\nos_name:\s*"+({os}[^"]+)""",
      """\\nagent_version:\s*"+({user_agent}[^"]+)""",
      """\ssizeBytes:\s*({bytes}\d+)""",
      """user\s*\{[^\}]+?sid:[^"]*?"+({user_sid}[^"\\]+)""",
      """user\s*\{(\\n|\\t|\\t)*\s+name:\s+[\\\/]?"*((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-]{1,40}\$?)))"""",
      """"app-username":"((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[\w\.\-]{1,40}\$?))\s*"""",
      """\ssha256:\s*[\\\/]?"+({hash_sha256}[^"\\]+)""",
      """\smd5:\s*[\\\/]?"+({hash_md5}[^"\\]+)""",
      """\spid:\s*({process_id}\d+)""",
      """path:\s+[\\\/]?"+({process_path}({process_dir}[^"]+?)[\\\/]*({process_name}[^"\\\/]+))[\\\/]*"""",
      """destinationAddress\s.*?address:\s*[\\\/]?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """destinationAddress\s.*?port:\s*({dest_port}\d+)""",
      """\sstatus:\s*({result}\w+)""",
      """(sourceAddress|\slocal)\s.*?port:\s*({src_port}\d{1,5})""",
      """(sourceAddress|\slocal)\s.*?address:\s*[\\\/]?"+(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?""",
      """sha1:\s*"*({hash_sha1}[^"]+)"""",
      """sizeBytes:\s*({bytes}\d+)""",
      """commandLine:\s*"({process_command_line}[^\{]+?)"\\n\s"""
    
}
```