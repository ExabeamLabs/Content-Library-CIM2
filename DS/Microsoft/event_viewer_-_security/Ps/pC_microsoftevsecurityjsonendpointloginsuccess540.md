#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-success-540"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """"event_id":540,""", """Successful Network Logon:""" ]
Fields = [
  """({event_name}Successful Network Logon)"""
  """"@timestamp"\s*:\s*"({time}.+?)""""
  """"(?:winlog\.)?computer_name"\s*:\s*"({host}[\w\-.]+?)""""
  """"event_id"\s*:\s*({event_code}\d+)"""
  """"user"\s*:\s*\{.*?"domain"\s*:\s*"({domain}.+?)""""
  """"user"\s*:\s*\{.*?"name"\s*:\s*"({user}[\w\.\-]{1,40}\$?)""""
  """"(param1|UserName)"\s*:\s*"({user}[\w\.\-]{1,40}\$?)\s*""""
  """"(param2|Domain)"\s*:\s*"({domain}.+?)\s*""""
  """"(param14|SourceNetworkAddress|source_ip)"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*""""
  """"(param7|Workstation|workstation_name)"\s*:\s*"({src_host_windows}.+?)\s*""""
  """"(param7|Workstation|workstation_name)"\s*:\s*"({src_host}[^"]+).*?Source Network Address:(\\t)*-[\\n\\t]+"""
  """"(param5|LogonProcess)"\s*:\s*"({auth_process}.+?)\s*""""
  """"(param6|AuthenticationPackage|authentication_package)"\s*:\s*"({auth_package}.+?)\s*""""
  """"(param3|LogonId|logon_id)"\s*:\s*"({login_id}.+?)\s*""""
  """"(param3|LogonId|logon_id)"\s*:\s*"\(([\dxA-F]+,)?({login_id}.+?)\)\s*""""
  """"(param4|LogonType)"\s*:\s*"({login_type}\d+)\s*""""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```