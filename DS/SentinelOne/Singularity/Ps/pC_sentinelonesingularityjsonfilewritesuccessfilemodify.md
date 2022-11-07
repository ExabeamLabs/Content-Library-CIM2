#### Parser Content
```Java
{
Name = sentinelone-singularity-json-file-write-success-filemodify
  Product = Singularity
  ParserVersion = v1.0.0
  Conditions = [ """"eventType": "File Modification"""", """"agentName":""", """"fileFullName":""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-threat-events.Fields}[
    """"fileSha1":\s*"({hash_sha1}[^"]+)""""
  ]

json-sentinelone-threat-events = {
    Vendor = SentinelOne
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Fields = [ 
      """"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""",
      """"eventType":\s*"({event_name}[^"]+)"""",
      """"agentName":\s*"({dest_host}[^"]+)"""",
      """"fileFullName":\s*"({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?))"""",
      """"processName":\s*"({process_name}[^"]+)"""",
      """"dstIp":\s*"({dest_ip}[A-Fa-f:\d.]+)"""",
      """"srcIp":\s*"({src_ip}[A-Fa-f:\d.]+)"""",
      """"processUser":\s*"(({domain}[^"\\]+)\\+)?({user}[^"]+)"""",
      """"agentDomain":\s*"({src_domain}[^"]+)""",
      """"agentComputerName":\s*"({src_host}[^"]+)"""
    
}
```