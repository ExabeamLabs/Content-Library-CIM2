#### Parser Content
```Java
{
Name = bitdefender-gz-json-alert-trigger-success-hd
  Conditions = [ """gravityzone:""", """"module":"hd"""" ]
  ParserVersion = "v1.0.0"

gravityzone-security-alert = {
    Vendor = Bitdefender
    Product = GravityZone
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    last_blocked_timeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
    Fields = [
      """"(timestamp|date|last_blocked)":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"(attack_type|aph_type|exploit_type)":"({alert_type}[^"]+)""",
      """"user":\{[^\}]*?"name":"(({email_address}[^"@]+@[^"@]+\.[^\]\s"\\,\|]+)|({user}[^"]+))"""",
      """"computer_name":"({host}[^"]+)""",
      """"computer_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"last_blocked":"({last_blocked_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"malware_name":"({alert_name}[^"]+)""",
      """"hash":"({hash_md5}[^"]+)""",
      """"(file_path|exploit_path)":"({malware_file_name}[^"]+)""",
      """"status":"({result}[^"]+)""",
      """"final_status":"({result}[^"]+)""",
      """"malware_type":"({category}[^"]+)""",
      """"count":({count}\d+)"""
    
}
```