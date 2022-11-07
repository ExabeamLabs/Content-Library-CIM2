#### Parser Content
```Java
{
Name = sentinelone-s-cef-http-session-success-visibility-1
  ParserVersion = v1.0.0
  Conditions = [
"""dproc=Deep Visibility Endpoint""",
"""destinationServiceName =SentinelOne""",
"""url:""",
"""http {"""
  ]
  Fields = ${SentinelOneParsersTemplates.sentinelone-activity.Fields} [
    """,({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)""",
    """url:\s*"+({url}(({protocol}[^:\\\/\s,"]+):\/*)?({web_domain}[^\\\/\s:,"\?]+)(:({dest_port}\d+))?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?)""""
]

sentinelone-activity = {

  Vendor = SentinelOne
  Product = Singularity
  TimeFormat = "epoch"
  Conditions = [
"""dproc=Deep Visibility Endpoint""",
"""destinationServiceName =SentinelOne""",
"""method:""",
"""http {"""
  ]
    Fields = [
      """\smillisecondsSinceEpoch:\s*({time}\d+)""",F
      """\\ncomputer_name:\s*"+({host}[^"]+)"""
      """\\nos_name:\s*"+({os}[^"]+)"""
      """\\nagent_version:\s*"+({user_agent}[^"]+)"""
      """\ssizeBytes:\s*({bytes}\d+)""",
      """user\s*\{[^\}]+?sid:[^"]*?"+({user_sid}[^"\\]+)""",
      """user\s*\{\\n\s+name:\s+\\?"*((NT AUTHORITY|({domain}[^\\"]+))\\+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^\\"]+))""",
      """"app-username":"((NT AUTHORITY|({domain}[^\\"]+))\\+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^"]+?))\s*"""",
      """\ssha256:\s*\\?"+({hash_sha256}[^"\\]+)""",
      """\smd5:\s*\\?"+({hash_md5}[^"\\]+)""",
      """\spid:\s*({process_id}\d+)""",
      """path:\s+\\?"+({process_path}({process_dir}[^"]+?)[\\\/]*({process_name}[^"\\\/]+))\\*"""",
      """destinationAddress\s.*?address:\s*\\?"+({dest_ip}[^\\"]+)""",
      """destinationAddress\s.*?port:\s*({dest_port}\d+)""",
      """\sstatus:\s*({result}\w+)""",
      """sourceAddress\s.*?port:\s*({src_port}\d+)""",
      """sourceAddress\s.*?address:\s*\\?"+({src_ip}[^"\\]+)""",
      """sha1:\s*"*({hash_sha1}[^"]+)""""
    
}
```