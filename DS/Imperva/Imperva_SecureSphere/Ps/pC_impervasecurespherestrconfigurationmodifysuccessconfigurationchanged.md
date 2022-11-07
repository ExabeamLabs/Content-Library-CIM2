#### Parser Content
```Java
{
Name = imperva-securesphere-str-configuration-modify-success-configurationchanged
  ParserVersion = "v1.0.0"
  Conditions = ["""|Imperva Inc""" , """SecureSphere""" , """cat=SystemEvent""" , """ConfigurationChanged|"""]

securesphere-system = {
  Vendor = Imperva
  Product = Imperva SecureSphere
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
     """\(({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d)""",
     """SecureSphere\|[^|]+?\|({operation}[^\|]+)\|({event_name}[^\|]+)\|({severity}[^\|]+)\|\s*suser=(({last_name}[^,]+),\s*({first_name}.+?)|({user}[^\s].+?))\srt"""
  ]
 }

}
#============================================== Start of ImpervaParsers section ==================================================================
ImpervaParsers = [
{
Name = "imperva-incapsula-cef-http-session-ddos"
Vendor = "Imperva"
Product = "Incapsula"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Incapsula|SIEMintegration|"""
"""|DDoS|"""
]
Fields = [
"""\Wstart=({time}\d+)"""
"""\Wsrc=({dest_ip}[A-Fa-f:\d.]+)"""
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
},

{
  Name = imperva-i-cef-http-session-siemintegration
  ParserVersion = v1.0.0  
  Vendor = Imperva
  Product = Incapsula
  TimeFormat = "epoch"
  Conditions = [ 
"""CEF:"""
"""|Incapsula|SIEMintegration|"""
"""deviceExternalId"""
""" ccode"""
]
  Fields = [
        """sip\\=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s""",
        """start\\=({time}\d+)""",
        """src\\=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s""",
        """sourceServiceName\\=({web_domain}.+?)\s+(\w+=|$)""",
        """act\\=({action}[A-Z_]+)\s""",
        """requestClientApplication\\=({user_agent}.+?)\s+(\w+\\=|$)""",
        """cn1\\=({http_response_code}\d+)\s""",
        """cpt\\=({src_port}\d+)\s""",
        """spt\\=({dest_port}\d+)\s""",
        """app\\=({protocol}[^|\s]+)\s""",
        """request\\=({uri_path}[^\s]+)\s""",
        """qstr\\=({uri_query}[^|]+)\\\\=""",
        """in\\=({bytes}\d+|$)\s""",
  ]

  DupFields = [ "uri_path->url" 
}
```