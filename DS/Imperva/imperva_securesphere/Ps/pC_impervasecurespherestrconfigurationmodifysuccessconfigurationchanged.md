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
},

{
  Name = imperva-incapsula-cef-http-session-siemintegration
  ParserVersion = v1.0.0  
  Vendor = Imperva
  Product = Imperva Incapsula
  TimeFormat = "epoch"
  Conditions = [ 
"""CEF:"""
"""|Incapsula|SIEMintegration|"""
"""deviceExternalId"""
""" ccode"""
]
  Fields = [
      """sip\\?=(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s""",
      """start\\?=({time}\d{13})""",
      """src\\?=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
      """sourceServiceName\\*=({web_domain}.+?)\s+(\w+\\?=|$)""",
      """act\\?=({action}[A-Z_]+)\s""",
      """requestClientApplication\\?=({user_agent}.+?)\s+(\w+\\?=|$)""",
      """cn1\\?=({http_response_code}\d+)\s""",
      """cpt\\?=({src_port}\d+)\s""",
      """spt\\?=({dest_port}\d+)\s""",
      """app\\?=({protocol}[^|\s%=]+)\s""",
      """request\\?=({uri_path}[^\s]+)\s""",
      """qstr\\?=({uri_query}[^|]+)\\\\=""",
      """in\\?=({bytes}\d+|$)\s""",      
  ]

  DupFields = [ "uri_path->url" 
}
```