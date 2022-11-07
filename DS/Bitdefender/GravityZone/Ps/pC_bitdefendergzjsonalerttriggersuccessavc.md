#### Parser Content
```Java
{
Name = bitdefender-gz-json-alert-trigger-success-avc
  ParserVersion = v1.0.0
  Conditions = [ """gravityzone:""", """"module":"avc"""" ]

gravityzone-security-alert = {
    Vendor = Bitdefender
    Product = GravityZone
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"(timestamp|date|last_blocked)":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"(attack_type|aph_type|exploit_type)":"({alert_type}[^"]+)""",
      """"user":\{[^\}]*?"name":"(({email_address}[^"@]+@[^"@]+)|({user}[^"]+))"""",
      """"computer_name":"({host}[^"]+)""",
      """"computer_ip":"({src_ip}[A-Fa-f:\d.]+)""",
      """"last_blocked":"({last_blocked_time}[^"]+)""",
      """"malware_name":"({alert_name}[^"]+)""",
      """"hash":"({hash_md5}[^"]+)""",
      """"(file_path|exploit_path)":"({malware_file_name}[^"]+)""",
      """"status":"({result}[^"]+)""",
      """"final_status":"({result}[^"]+)""",
      """"malware_type":"({category}[^"]+)""",
      """"count":({count}\d+)"""
    
}
```