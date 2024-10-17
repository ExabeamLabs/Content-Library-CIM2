#### Parser Content
```Java
{
Name = "checkpoint-vsec-kv-vpn-login-success-ipchanged"
Vendor = "Check Point"
Product = "Check Point vSEC Virtual Edition"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
"""ProductName: Connectra;"""
"""ip changed"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+((\+|\-)\d\d:\d\d)?)"""
"""({host}[\w.\-]+)\s+CPLogToSyslog:"""
"""\WOriginSicName:\s*CN=({host}[\w.\-]+),O="""
"""\WAction:\s*(|({action}[^;]+?));"""
"""\Wuser:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*;"""
"""\Wuser:\s*({full_name}.+?)\s*\(({account}.+?)\)"""
"""\Wsrc:\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?);"""
"""\WProductName:\s*(|({app}[^;]+?));"""
"""\Wassigned_IP::\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\,orig=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
DupFields = [
"action->event_name"
"account->user"
]
ParserVersion = "v1.0.0"


}
```