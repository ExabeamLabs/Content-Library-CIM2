#### Parser Content
```Java
{
Name = imperva-securesphere-cef-database-login-success-login
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF""", """|cat=Audit""" , """|EventId=""" , """|Policy=""" , """|SourceApplication=""", """|EventType=Login"""]

securesphere-db-activity= {
  Vendor = Imperva
  Product = Imperva SecureSphere
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """rt=({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """EventId=({alert_id}[^\|]+)"""
    """Policy=({policy_name}[^\|]+)"""
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """spt=({src_port}\d+)"""
    """OSUser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """dpt=({dest_port}\d+)"""
    """duser=(({domain}[^\\\s]+)\\+)?({account}({db_user}[^\s\|]+))"""
    """UserGroup=({group_name}[^\|]+)"""
    """\WserviceName ="(|({service_name}[^"\|]+))"""
    """HostName =({host}[^\|]+)"""
    """Schema=({db_schema}[^\|]+)"""
    """Database=({db_name}[^\|]+)"""
    """EventType=({event_category}[^\|]+)"""
    """ApplicationName =({app}[^\|]+)"""
    """Operation=({operation}[^\|]+)"""
    """RawQuery=({db_query}[^\|\$]+)"""
    """Object=({object}[^\|]+)"""
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
"""\Wsrc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
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
      """sip\\?=(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s""",
      """start\\?=({time}\d{13})""",
      """src\\?=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
      """sourceServiceName\\*=({web_domain}.+?)\s+(\w+\\?=|$)""",
      """act\\?=({action}[A-Z_]+)\s""",
      """requestClientApplication\\?=({user_agent}.+?)\s+(\w+\\?=|$)""",
      """requestClientApplication\\+=({user_agent}.+?)\s+(\w+\\?=|$)""",
      """cn1\\?=({http_response_code}\d+)\s""",
      """cpt\\?=({src_port}\d+)\s""",
      """spt\\?=({dest_port}\d+)\s""",
      """app\\?=({protocol}[^|\s%=]+)\s""",
      """request\\?=({url}({uri_path}[^\s]+))\s""",
      """qstr\\?=({uri_query}[^|]+?)\s\w+\\?=""",
      """in\\?=({bytes}\d+|$)\s""",
      """\|Incapsula\|SIEMintegration\|([^\|]*?\|){2}({attack}[^\|]+)\|""",
      """requestMethod\\?=({method}\w+)""",
      """fileType\\?=({file_type}[^\s]+)""",
      """filePermission\\?=({permission}[^\s]+)""",
      """cs9\\?=({rule}[^=]+)\s\w+\\?=""",
      """ccode\\?=({country_code}[^=]+)\s""",
      """cicode\\?=({city}[^=]+)\s\w+\\?="""
  
}
```