#### Parser Content
```Java
{
Name = "cisco-ise-cef-endpoint-login-success-accounting"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Cisco ISE|"""
"""|TACACS+ Accounting START|"""
"""CISE_TACACS_Accounting"""
""" dvc="""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sahost=({host}[\w.-]+)\s"""
"""({event_name}CISE_TACACS_Accounting)"""
"""\|Cisco ISE\|[^\|]*\|({event_code}\d+)"""
"""\sdvchost=({dest_host}[\w.-]+)\s"""
"""\sdvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
"""\samac=({src_mac}[\w-]+)\s"""
"""({auth_type}TACACS\+ Accounting)"""
]
DupFields = [
"host->auth_server"
]
ParserVersion = "v1.0.0"


}
```