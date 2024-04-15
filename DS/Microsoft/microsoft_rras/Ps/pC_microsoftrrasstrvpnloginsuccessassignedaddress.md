#### Parser Content
```Java
{
Name = "microsoft-rras-str-vpn-login-success-assignedaddress"
Vendor = "Microsoft"
Product = "Microsoft RRAS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""RoutingDomainID-"""
"""CoID= {"""
"""has been assigned address"""
]
Fields = [
"""CoID=\{({session_id}[^\{\}]+?)\}"""
""":\s*The user (({domain}[^\\\/]+?)[\\\/]+)?({user}[^\\\/]+?) connected on port"""
"""has been assigned address ({src_translated_ip}[a-fA-F\d.:]+)"""
]
ParserVersion = "v1.0.0"


}
```