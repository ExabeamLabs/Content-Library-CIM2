#### Parser Content
```Java
{
Name = "fortinet-utm-cef-endpoint-authentication-fail-ntlmauth"
Vendor = "Fortinet"
Product = "Fortinet UTM"
TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
Conditions = [
"""CEF:0|Fortinet|Fortigate"""
"""status\="failure""""
"""action\="NTLM-auth""""
""" logdesc\="""
]
Fields = [
"""date\\=({time}\d\d\d\d-\d\d-\d\d time\\=\d\d:\d\d:\d\d)"""
"""devname\\="*({host}[^"]+?)"*(\s+\w+\\=|\s*$)"""
"""\ssrcip\\="?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdstip\\="?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\suser\\="*(N\/A|({user}[^"]+?))"*(\s+\w+\\=|\s*$)"""
"""\slogdesc\\="({event_name}[^"]+)"""
"""\sdevid\\="({dest_host}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```