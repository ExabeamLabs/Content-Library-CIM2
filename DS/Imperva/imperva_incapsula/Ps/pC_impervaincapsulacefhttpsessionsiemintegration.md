#### Parser Content
```Java
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
      """request\\?=({uri_path}[^\s]+)\s""",
      """qstr\\?=({uri_query}[^|]+?)\s\w+\\?=""",
      """in\\?=({bytes}\d+|$)\s""",
      """\|Incapsula\|SIEMintegration\|([^\|]*?\|){2}({attack}[^\|]+)\|""",
      """requestMethod\\?=({method}\w+)""",
      """fileType\\?=({file_type}[^\s]+)""",
      """filePermission\\?=({permission}[^\s]+)""",
      """cs9\\?=({rule}[^=]+)\s\w+\\?=""",
      """ccode\\?=({country_code}[^=]+)\s""",
      """cicode\\?=({city}[^=]+)\s\w+\\?="""
  ]

  DupFields = [ "uri_path->url" ]


}
```