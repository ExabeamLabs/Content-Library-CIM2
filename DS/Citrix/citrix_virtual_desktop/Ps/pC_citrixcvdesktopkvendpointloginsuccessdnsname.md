#### Parser Content
```Java
{
Name = "citrix-cvdesktop-kv-endpoint-login-success-dnsname"
Vendor = "Citrix"
Product = "Citrix Virtual Desktop"
TimeFormat = "MM/dd/yyyy HH:mm:ss z"
Conditions = [
""" DNSName =\""""
""" HostedMachineName =\""""
""" MachineSummaryState=\""""
]
Fields = [
"""\sStartTime=\"({time}[^\"]+?)\""""
"""\sDNSName =\"({dest_host}[^\"]+?)\""""
"""\sIPAddress=\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
"""\sLaunchedViaHostName =\"({src_host}[^\"]+?)\""""
"""\sLaunchedViaIP=\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
"""\sClientName =\"({src_host}(?!HTML-)[^\"]+?)\""""
"""\sClientAddress=\"({src_ip}(?!127\.0\.0\.1|0\.0\.0\.0|::0)[^\"]+?)\""""
"""\sProtocol=\"({login_type_text}[^\"]+?)\""""
"""\sCatalogName =\"({catalog}[^\"]+?)\""""
"""\sUserName =\"(({domain}[^\"]+)\\)?({user}[^\"]+?)\""""
"""\sUserSID=\"({user_sid}[^\"]+?)\""""
]
DupFields = [
"dest_ip->host"
"dest_host->host"
]
ParserVersion = "v1.0.0"


}
```