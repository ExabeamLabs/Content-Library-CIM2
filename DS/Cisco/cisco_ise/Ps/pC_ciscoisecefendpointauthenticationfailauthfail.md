#### Parser Content
```Java
{
Name = "cisco-ise-cef-endpoint-authentication-fail-authfail"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Cisco ISE|"""
"""|Authentication failed|"""
"""Access and Identity Management"""
""" app=Tacacs """
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sahost=({host}[\w.-]+)\s"""
"""({event_name}User authentication failed)"""
"""\|Cisco ISE\|[^\|]*\|({event_code}\d+)"""
"""\sdvchost=({dest_host}[\w.-]+)\s"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
"""\sshost=({src_host}[\w.-]+)\s"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
"""\samac=({src_mac}[\w-]+)\s"""
"""\ssuser=(({email_address}[^\s@]+@[^\s@]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
]
DupFields = [
"host->auth_server"
]
ParserVersion = "v1.0.0"


}
```