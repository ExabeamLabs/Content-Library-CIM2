#### Parser Content
```Java
{
Name = sentinelone-singularityp-sk4-registry-delete-regvaluedelete-1
  ParserVersion = "v1.0.0"
  Product = Singularity Platform
  Conditions = [ """"SentinelOne"""", """Deep Visibility Endpoint""", """regValueDelete {""" ]
  Fields = ${DLSentinelOneParsersTemplates.sentinelone-activity-dl.Fields} [
    """({event_name}regValueDelete)""",
  ]

sentinelone-activity-dl {
    Vendor = SentinelOne
    TimeFormat = "epoch"
    Fields = [
      """\\ncomputer_name:\s*"+({dest_host}[^"]+)"""
      """\smillisecondsSinceEpoch:\s*({time}\d{13})""",
      """\\nos_name:\s*"+({os}[^"]+)"""
      """\\nagent_version:\s*"+({user_agent}[^"]+)"""
      """\ssizeBytes:\s*({bytes}\d+)""",
      """user\s*\{.+?sid:.*?"+({user_sid}[^"\\]+)""",
      """user\s*\{\\n\s+name:\s+\\?"*(((NT AUTHORITY|({domain}[^\\"]+))\\\\)?(SYSTEM|NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
      """\ssha256:\s*\\?"+({hash_sha256}[^"\\]+)""",
      """\ssha1:\s*"+({hash_sha1}[^"]+)""",
      """\smd5:\s*\\?"+({hash_md5}[^"\\]+)""",
      """\scommandLine:\s*\\?"\s*({process_command_line}.+?)\s*"\\n""",
      """\spid:\s*({process_id}\d+)""",
      """path:\s+\\?"+({process_path}({process_dir}[^"]+?)[\\\/]*({process_name}[^"\\\/]+))\\*"""",
      """\ssource.*?node.+?value:\s*\\?"+({src_host}[^"\\]+)""",
      """destinationAddress\s.*?address:\s*\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """destinationAddress\s.*?port:\s*({dest_port}\d+)""",
      """\sstatus:\s*({result}\w+)""",
      """sourceAddress\s.*?port:\s*({src_port}\d+)""",
      """sourceAddress\s.*?address:\s*\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    
}
```