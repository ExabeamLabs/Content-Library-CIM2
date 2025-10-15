#### Parser Content
```Java
{
Name = "trendmicro-vone-cef-user-create-adduseraccount"
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Trend Micro|Trend Vision One|""", """|900003|""", """ cs3=Add user account""" ]
   Fields = ${TrendMicroParserTemplates.trendmicro-vision-one-account-audit.Fields}[
     """'User account':\s*'(({full_name}[^'\s]+\s+[^\s']+)|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'"""
   ]
 } 
]
#============================================== End of TrendMicroParsers section ==================================================================

#============================================== Start of TrendMicroParsersDL section ==================================================================
TrendMicroParsersDL = [

${TrendMicroParserTemplates.trendmicro-ds-ossecevents}{
  Name = trendmicro-ds-json-group-modify-success-4735
  ParserVersion = v1.0.0
  Conditions = [ """"OSSEC_Log""", """"Origin\":0""", """"EventType\":\"LogInspectionEvent""", """A security-enabled local group was changed""", """4735""" ]
  Fields = ${TrendMicroParserTemplates.trendmicro-ds-ossecevents.Fields}[
    """({event_name}A security-enabled local group was changed)""",
    """Group:\s+Security ID:\s+({group_id}[^\s]+)""",
    """Group:.+?(Group|Account) Name:\s+({group_name}.+?)?\s+(Group|Account) Domain:""",
    """Group:.+?(Group|Account) Domain:\s+({group_domain}[^\s]+)"""
  ]

trendmicro-vision-one-account-audit = { 
  Vendor = Trend Micro
  Product = Vision One
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """CEF:([^\|]*\|){4}({event_code}[^|]+)""",
    """CEF:([^\|]*\|){5}({event_category}[^|]+)""",    
    """cat=((?i)Unknown|({category}[^=,]+))(\s*,\S+)?\s+\w+=""",
    """({app}Trend Vision One)""",
    """ \d\d:\d\d:\d\d ({host}[\w.-]+)\s""",
    """ cn1=({result}\d)""", 
    """ cs1=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^=]+?))((\s+\w+=)|\s*$)""",
    """ cs2=({role}[^=]+?)((\s+\w+=)|\s*$)""",
    """ cs3=({operation}({event_name}[^=]+?))((\s+\w+=)|\s*$)""",
    """ msg=\{({additional_info}[^=]+?)\}\s*(\s*$|(\s+\w+=))"""
  
}
```