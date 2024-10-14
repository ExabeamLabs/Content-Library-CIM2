#### Parser Content
```Java
{
Name = "juniper-ps-cef-vpn-logout-success-juniper"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Juniper|"""
"""|Closed connection|"""
""" bytes read """
""" bytes written """
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdst=\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wsuser=(System|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\Wduser=({dest_user}[^\s]+)"""
"""\Wshost=({src_host}[\w\-.]+)"""
"""\Wahost=({dest_host}.*?)\s\w+=""",
"""\Wafter\s+({session_duration}\d+)\s+seconds""",
"""\Wwith\s+({bytes_in}\d+)\s+bytes read""",
"""\Wand\s+({bytes_out}\d+)\s+bytes written"""
"""\Wmsg=({additional_info}.+?)\s+end=""",
"""Closed connection to=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",

]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```