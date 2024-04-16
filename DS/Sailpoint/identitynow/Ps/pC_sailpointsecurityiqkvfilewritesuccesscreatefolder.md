#### Parser Content
```Java
{
Name = "sailpoint-securityiq-kv-file-write-success-createfolder"
Conditions = [
  """| applicationtype : Netapp - CIFS |"""
  """actiontype : Create Folder"""
]
ParserVersion = "v1.0.0"

s-sailpoint-activity.Fields} [
    """exa_json_path=$.application,exa_regex=((?i:null|NONE)|({app}[^"]+))""",
    """exa_json_path=$.info,exa_regex=((?i:null|NONE)|({additional_info}[^"]+))"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = sailpoint-iiq-json-user-password-modify-success-target
  ParserVersion = "v1.0.0"
  Vendor = Sailpoint
  Product = IdentityNow
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"ATTRIBUTE_NAME""", """"password""", """"ACCOUNT_NAME""", """"APPLICATION""", """"OWNER""", """"ACTION""", """"TARGET""", """"SOURCE""" ]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
    """"ACCOUNT_NAME\\?":\\?"(({user_dn}(((CN|cn|uid)=[^"]+?),)?(({user_ou}(OU|ou)[^"]+?)?(DC|dc)=[\w-]+))|({account_id}[^"]+?)\\?")""",
    """"TARGET\\?":\\?"(({email_address}[^@"]+@[^"]+?)|({user}[\w\.\-]{1,40}\$?))\\?"""",
    """"SOURCE\\?":\\?"(({email_address}[^@"]+@[^"]+?)|({user}[\w\.\-]{1,40}\$?))\\?"""",
    """"APPLICATION\\?":\\?"({app}[^"]+?)\\?"""",
    """"ACTION\\?":\\?"({operation}[^"]+?)\\?""""
  ]
  DupFields = [ "operation->event_name" 
}
```