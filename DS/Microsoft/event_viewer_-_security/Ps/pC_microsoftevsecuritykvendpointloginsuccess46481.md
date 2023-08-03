#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-success-4648-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """__li_source_path=""", """A logon was attempted using explicit credentials""","""eventid="4648"""" ]
  Fields = [ 
    """({event_name}A logon was attempted using explicit credentials)""",
    """__li_source_path="({host}[^"]+)"""",
    """({event_code}4648)""",
    """Subject:\s+Security ID:\s+({user_sid}[^\s]+)""",
    """Subject:.+?Account\sName:\s+(?:-|({user}[\w\.\-]{1,40}\$?))\s+Account\sDomain:\s+(?:-|({domain}[^\s]+))\s+Logon\sID:\s+({login_id}[^\s]+)\s+""",
    """Used:\s+Account\sName:\s+({dest_user}[^\s]+)\s+Account\sDomain:\s+({dest_domain}[^\s]+)\s+"""
    """Target\sServer\sName:\s+({dest_host}[^\s]+)""",
    """Process ID:\s+({process_id}\w+)\s+Process Name:""",
    """Process Name:\s+(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?)))\s+Network Information:""",
    """Network Address:\s+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """Additional Information:\s+({dest_service_name}[^\s]+)\s+Process Information:"""
  ]
  ParserVersion = "v1.0.0"


}
```