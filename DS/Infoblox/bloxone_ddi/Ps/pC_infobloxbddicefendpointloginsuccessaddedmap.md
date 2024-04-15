#### Parser Content
```Java
{
Name = "infoblox-bddi-cef-endpoint-login-success-addedmap"
Vendor = "Infoblox"
Product = "BloxOne DDI"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""Added Forward Map"""
"""dhcpd"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""sntdom=({dest_host}[^\s]+)"""
"""\ssrc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
"dest_host->user"
]
ParserVersion = "v1.0.0"


}
```