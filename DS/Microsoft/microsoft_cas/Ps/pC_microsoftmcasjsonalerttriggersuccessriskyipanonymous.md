#### Parser Content
```Java
{
Name = microsoft-mcas-json-alert-trigger-success-riskyipanonymous
Product = "Microsoft CAS"
Conditions = [
  """"category":"""
  """"MCAS_ALERT_ANUBIS_DETECTION_RISKY_IP_ANONYMOUS""""
  """"title":"""
  """"vendor":"""
  """"Microsoft""""
  """"provider":"""
  """"MCAS""""
]
ParserVersion = "v1.0.0"

cef-defender-atp-3.Fields} [
    """"FolderPath"+:\s*"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
    """DeviceName"+:\s*"+({dest_host}({host}[\w\-.]+))""",
    """MD5"+:"+({hash_md5}[^"]+)""",
    """"SHA1"+:(null|"+({hash_sha1}[^",]+)"+),""",
    """"SHA256"+:(null|"+({hash_sha256}[^",]+)"+),"""
    """"InitiatingProcessAccountName"+:\s*"+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  
}
```