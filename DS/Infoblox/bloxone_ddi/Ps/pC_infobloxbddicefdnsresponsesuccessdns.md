#### Parser Content
```Java
{
Name = "infoblox-bddi-cef-dns-response-success-dns"
Vendor = "Infoblox"
Product = "BloxOne DDI"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""|Infoblox|"""
"""app=DNS"""
"""InfobloxDNSView="""
"""InfobloxDNSQType="""
]
Fields = [
     """src=(\s|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
     """dst=(\s|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
     """spt=(\s|({src_port}\d+))""",
     """proto=(\s|({protocol}[^\s]+))""",
     """app=({app}[^\s]+)""",
     """InfobloxDNSRCode=({dns_response_code}[^\s]+)\s""",
     """InfobloxDNSQType=(\s|({dns_query_type}[^\s]+))""",
     """destinationDnsDomain=(\s|({dns_query}[^\s]+))""",
     """msg=(\s|({additional_info}.+?));\s\.\s32768""",

]
ParserVersion = "v1.0.0"


}
```