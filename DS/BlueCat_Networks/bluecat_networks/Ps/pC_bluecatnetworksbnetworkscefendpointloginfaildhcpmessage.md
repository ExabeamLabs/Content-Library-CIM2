#### Parser Content
```Java
{
Name = "bluecatnetworks-bnetworks-cef-endpoint-login-fail-dhcpmessage"
Vendor = "BlueCat Networks"
Product = "BlueCat Networks"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|BCN|BDDS_DHCP|"""
"""|DHCP_Message|DHCP message|"""
"""shost="""
"""src="""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[\w.\-]+)"""
"""\scat=(?:|({category}.+?))\s\w+="""
"""\sshost=({dest_host}[^\s]+)"""
"""\ssrc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
"dest_host->user"
]
ParserVersion = "v1.0.0"


}
```