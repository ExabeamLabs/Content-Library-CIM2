#### Parser Content
```Java
{
Name = akamai-guardicore-cef-app-activity-userauth
    Vendor = Akamai 
    Product = Akamai Guardicore
    TimeFormat = "yyyy-MM-dd'T'HH:mmZ"
    Conditions = [ """CEF:""", """Guardicore|Centra""", """Audit Record""", """act=User authentication"""]
    Fields = [
      """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\dZ)""",
      """CEF:\d+\|([^\|]+\|){4}({event_name}[^\|]+)""", 
      """CEF:\d+\|([^\|]+\|){3}({category}[^\|]+)""",
      """act=({action}[^=]+)\s+\w+=""",
      """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\ssuser=([^\\\s]+?\\)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\s\w+=""",
      """\Wrequest=({request}.+?)\s+(\w+=|$)""",
      """msg=({additional_info}.+?)\s+(\w+=|$)"""
    ]
    ParserVersion = v1.0.0
  } 

${LiquidFilesParserTemplates.Liquid-json-template}{
  Name = "liquidfiles-l-json-file-upload-attachment"
  ParserVersion = v1.0.0
  Conditions = [ """liquidfiles[""", """"message":"Attachment """, """"filename":"""" ]


}
```