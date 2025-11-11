#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-success-4624-3"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""An account was successfully logged on"""
""""event_id":"4624""""
""""new_logon-LogonID":""""
]
Fields = [
"""({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))""""
""""host":"({host}[\w\-.]+)\s*"""
"""({event_name}An account was successfully logged on)"""
"""({event_code}4624)"""
""""logon_type":"\s*({login_type}\d+)"""
""""new_logon-AccountName":"\s*({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*""""
""""new_logon-AccountDomain":"\s*({domain}[^"]+)\s*""""
""""process_information-ProcessName":"(-|\s*({process_path}[^"]+))\s*""""
""""network_information-WorkstationName":"\s*(-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host_windows}({src_host}[\w\-.]+)))\s*""""
""""network_information-SourceNetworkAddress":"\s*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*""""
""""detailed_authentication_information-LogonProcess":"\s*({auth_process}[^"]+)\s*""""
""""detailed_authentication_information-AuthenticationPackage":"\s*({auth_package}[^"]+)\s*""""
""""new_logon-LogonID":"\s*({login_id}[^"]+)\s*""""
""""new_logon-SecurityID":"\s*({user_sid}[^"]+)\s*""""
""""cmpny.source.ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""subject-SecurityID":"\s*({subject_sid}[^"]+)\s*""""
"""KeyLength":"\s*({key_length}\d+)\s*""""
]
ParserVersion = "v1.0.0"


}
```