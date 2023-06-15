#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-success-552-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"event_id":552""", """Logon attempt using explicit credentials:""", """"@timestamp"""" ]
  Fields = [
    """({event_name}Logon attempt using explicit credentials)""",
    """"@timestamp"\s*:\s*"({time}.+?)"""",
    """"(?:winlog\.)?computer_name"\s*:\s*"({host}.+?)"""",
    """"(param8|Dest_host)"\s*:\s*"(-|({dest_host}.+?))\s*"""",
    """"(param9|Dest_Service)"\s*:\s*"(-|({dest_service_name}.+?))\s*"""",
    """({event_code}552)""",
    """"host":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"(param11|SourceNetworkAddress|source_ip)"\s*:\s*"(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*"""",
    """"user"\s*:\s*\{.*?"domain"\s*:\s*"({domain}.+?)"""",
    """"(param1|UserName)"\s*:\s*"(-|({user}.+?))\s*"""",
    """"(param2|Target Domain|domain)"\s*:\s*"({domain}.+?)\s*"""",    
    """"(param7|Target Logon GUID)"\s*:\s*"(-|({account_login_guid}.+?))\s*"""",
    """"(param10|process_id)"\s*:\s*"(-|({process_id}.+?))\s*"""",
    """"(param5|Target User Name)"\s*:\s*"(-|({dest_user}.+?))\s*"""",
    """"(param6|Target Domain)"\s*:\s*"(-|({dest_domain}.+?))\s*"""",
    """"(param3|Logon ID|logon_id)"\s*:\s*"(-|({login_id}.+?))\s*"""",
    """"(param3|Logon ID|logon_id)"\s*:\s*"\(([\dxA-F]+,)?(-|({login_id}.+?)\))\s*"""",
    """"(param4|Logon GUID)"\s*:\s*"(-|({user_login_guid}.+?))"""",
    """record_number"\s*:\s*"({event_id}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```