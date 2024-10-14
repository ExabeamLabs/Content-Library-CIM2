#### Parser Content
```Java
{
Name = "beyondtrust-sra-kv-app-login-fail-status"
ParserVersion = "v1.0.0"
Vendor = "BeyondTrust"
Product = "BeyondTrust Secure Remote Access"
TimeFormat = "epoch_sec"
Conditions = [
""";status=failure;"""
""";target="""
""";when="""
""";who_ip="""
""";who="""
"""event=login"""
]
Fields = [
"""\s({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]\d+:\d+)\s+({host}[\w\-.]+)\s"""
"""\Wwhen=({time}\d{10})"""
"""\Wevent=({operation}[^;]+?)\s*;"""
"""\Wsite=({app}[^;]+)"""
"""\Wstatus=({result}[^;"]+?)\s*(;|"|$)""",
"""\Wtarget=({object}[^;]+?)\s*;"""
"""\Wwho_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wwho=[^;\(]*?\((({domain}[^;\s\)@\\\/]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s|;|\))"""
"""\Wwho=[^;\(]*?\(({email_address}[^;\s\)@\\\/]+@[^;\s\)@\\\/]+)(\s|;|\))"""
"""\Wusername=(({domain}[^;\s\)@\\\/]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s|;|\))"""
"""\Wusername=({email_address}[^;\s\)@\\\/]+@[^;\s\)@\\\/]+)(\s|;|\))"""
]


}
```