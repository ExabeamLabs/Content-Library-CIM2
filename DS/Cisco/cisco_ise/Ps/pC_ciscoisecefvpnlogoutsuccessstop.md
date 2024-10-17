#### Parser Content
```Java
{
Name = "cisco-ise-cef-vpn-logout-success-stop"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "epoch"
ParserVersion = "v1.0.0"
Conditions = [
"""CEF:"""
"""|Cisco ISE|"""
"""|RADIUS Accounting stop request|"""
""" act=Stop """
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sahost=({host}[\w.-]+)\s"""
"""\sdvchost=({dest_host}[\w.-]+)\s"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
"""\sshost=({src_host}[\w.-]+)\s"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
"""\samac=({src_mac}[\w-]+)\s"""
"""\ssuser=(({email_address}[^\s@]+@[^\s@]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""({event_name}RADIUS Accounting stop request)"""
"""\|Cisco ISE\|[^\|]*\|({event_code}\d+)"""
"""Acct Session Time:\s*({session_duration}\d+),"""
"""\scs5=({session_id}[^\s=]+)"""
"""\sout=({bytes_out}\d+)"""
"""\sin=({bytes_in}\d+)"""
]


}
```