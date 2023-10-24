#### Parser Content
```Java
{
Name = "juniper-ps-cef-vpn-login-success-agentloginsucceededfor"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Agent login succeeded for"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[^\s]+)"""
"""\ssuser=({user}[\w\.\-]{1,40}\$?)\s+sproc="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sspriv=({resource}.+?)\s+\w+="""
"""\sahost=({dest_host}.*?)\s+\w+="""
"""\sagt=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\scs6=({realm}.*?)\s+\w+=.*?cs6Label=Group Name"""
]
DupFields = [
"user->account"
]
ParserVersion = "v1.0.0"


}
```