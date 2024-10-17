#### Parser Content
```Java
{
Name = "symantec-csp-json-endpoint-login-success-userloggedin"
Conditions = [
"""SVA_IP_ADDRESS: """
""" USER_NAME:"""
"""User Logged in"""
]
ParserVersion = "v1.0.0"

gravityzone-security-alert = {
    Vendor = Bitdefender
    Product = GravityZone
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    last_blocked_timeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
    Fields = [
      """"(timestamp|date|last_blocked|created)":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"(attack_type(s)?|aph_type|exploit_type)":\[?"({alert_type}[^"]+)""",
      """"user":\{[^\}]*?"name":"(({email_address}[^"@]+@[^"@\.]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@"\.]+))?)"""",
      """"username":"(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
      """"user_sid":"({user_sid}[^"]+)"""",
      """"computer_name":"({host}[^"]+)""",
      """"computer_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"last_blocked":"({last_blocked_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"(detection_name|malware_name)":"({alert_name}[^"]+)""",
      """"hash":"({hash_md5}[^"]+)""",
      """"(file_path|exploit_path)":"({malware_file_name}[^"]+)""",
      """"main_action":"({result}[^"]+)"""",
      """"status":"({result}[^"]+)""",
      """"final_status":"({result}[^"]+)""",
      """"malware_type":"({category}[^"]+)""",
      """"count":({count}\d+)"""
      """"severity":"({alert_severity}[^"]+)"""",
      """"incident_id":"({alert_id}[^"]+)"""",
      """"process_command_line":"({process_command_line}[^$]+?)","\w+""",
      """"process_path":"({process_path}({process_dir}[^"]+?)[\\\/]+({process_name}[^"\\\/]+))"""",
      """"protocol_id":"({protocol}\d+)""""
    
}
```