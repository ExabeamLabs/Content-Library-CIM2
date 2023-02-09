#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-defenseevasion-1
Product = "Microsoft Defender for Endpoint"
Conditions = [
  """"category":"""
  """"DefenseEvasion""""
  """"title":"""
  """"vendor":"""
  """"Microsoft""""
  """"provider":"""
  """"Microsoft Defender ATP""""
]
ParserVersion = "v1.0.0"

cef-defender-atp.Fields} [
    """"FolderPath"+:\s*"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
    """DeviceName"+:\s*"+({dest_host}({host}[^"\.]+)?[^"]+)""",
    """MD5"+:"+({hash_md5}[^"]+)""",
    """"SHA1"+:(null|"+({hash_sha1}[^",]+)"+),""",
    """"SHA256"+:(null|"+({hash_sha256}[^",]+)"+),"""
  
}
```