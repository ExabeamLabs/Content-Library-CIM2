#### Parser Content
```Java
{
Name = "cimtrak-c-kv-file-read-success-filedeleted"
Conditions = [
"""CTK:"""
"""|Cimcor|CimTrak|"""
"""|File Deleted|"""
]
ParserVersion = "v1.0.0"
}  
 
 {
  Name = onespan-dp-kv-endpoint-authentication-success-sourcelocation
  Vendor = OneSpan
  Product = Digipass for Apps
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """Source Location """, """Event:""", """AMID:""" ]
  Fields = [
    """Timestamp:\s({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
    """Event:\s+\[[^\]]+\]\s({event_name}[^:]+)\.\s\w+:""",
    """User ID\s*:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\}|,)""",
    """Domain( Name)?\s*:\s*({domain}[^\},]+)(\}|,)""",
    """Source Location[^=]+=\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```