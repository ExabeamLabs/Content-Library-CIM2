#### Parser Content
```Java
{
Name = "imperva-incapsula-cef-http-session-ddos"
Vendor = "Imperva"
Product = "Imperva Incapsula"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Incapsula|SIEMintegration|"""
"""|DDoS|"""
]
Fields = [
"""\Wstart=({time}\d{13})"""
"""\Wsrc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wact=({action}.+?)\s+(\w+=|$)"""
"""\Wapp=({protocol}.+?)\s+(\w+=|$)"""
"""\Wref=({referrer}.+?)\s+(\w+=|$)"""
"""\WsourceServiceName =({web_domain}.+?)\s+(\w+=|$)"""
"""\WrequestClientApplication=({user_agent}.+?)\s+(\w+=|$)"""
"""\Wccode=({country_code}.+?)\s+(\w+=|$)"""
"""\WCustomer=({customer}.+?)\s+(\w+=|$)"""
"""\Wrequest=({url}.+?)\s+(\w+=|$)"""
"""\WrequestMethod=({method}.+?)\s+(\w+=|$)"""
"""\Wdproc=({category}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```