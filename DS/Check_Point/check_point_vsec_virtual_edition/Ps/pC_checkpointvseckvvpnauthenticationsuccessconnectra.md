#### Parser Content
```Java
{
Name = "checkpoint-vsec-kv-vpn-authentication-success-connectra"
Vendor = "Check Point"
Product = "Check point vSEC Virtual Edition"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
"""ProductName: Connectra;"""
"""Action: authcrypt;"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+((\+|\-)\d\d:\d\d)?)"""
"""({host}[\w.\-]+)\s+CPLogToSyslog:"""
"""\WOriginSicName:\s*CN=({host}[\w.\-]+),O="""
"""\WAction:\s*(|({action}[^;]+?));"""
"""\Wuser:\s*({user}[^;\(\)]+?)\s*;"""
"""\Wuser:\s*({full_name}.+?)\s*\(({account}.+?)\)"""
"""\Wsrc:\s*(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?);"""
"""\WProductName:\s*(|({app}[^;]+?));"""
"""\Wauth_method:\s*(|({auth_method}[^;]+?));"""
"""\Wos_name:\s*(|({os}[^;]+?));"""
"""\Wstatus:\s*(|({result}[^;]+?));"""
"""\Whost_ip:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
"action->event_name"
"account->user"
]
ParserVersion = "v1.0.0"


}
```