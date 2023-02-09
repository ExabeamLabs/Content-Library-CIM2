#### Parser Content
```Java
{
Name = unix-unix-json-user-switch-success-userstart
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"type":"user_start""""
  """PAM:session_open"""
  """"result":"success""""
]
Fields = [
  """"@timestamp":"({time}[^"]+)"""
  """"name_map":\{.*?"uid":"(|({user}[^"]+))""""
  """"user":\{.*?"uid":"({user_id}\d+)""""
  """"pid":"({process_id}\d+)"""
  """"process":\{.*?"exe":"(|({process_command_line}({process_dir}[^"]+\/).*?))""""
  """"data":\{.*?"acct":"(|({dest_user}[^"]+))""""
  """"host":\{.*?"name":"(|({host}[^"]+))""""
]
DupFields = [
  "host->dest_host", "dest_user->account"
]
ParserVersion = "v1.0.0"


}
```