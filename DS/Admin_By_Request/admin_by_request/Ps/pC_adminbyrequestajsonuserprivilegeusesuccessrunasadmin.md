#### Parser Content
```Java
{
Name = adminbyrequest-a-json-user-privilege-use-success-runasadmin
  Vendor = Admin By Request
  Product = Admin By Request
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ExtractionType = json
  Conditions = [ """"type":"Run As Admin"""" , """"elevatedApplications":""", """"approvedBy":""", """"traceNo":"""" ]
  Fields = [
    """exa_json_path=$.requestTime,exa_field_name=time""",
    """exa_json_path=$.user.account,exa_regex=(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
    """exa_json_path=$.user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.user.fullName,exa_field_name=full_name""",
    """exa_json_path=$.computer.name,exa_field_name=host""",
    """exa_json_path=$.computer.model,exa_field_name=additional_info""",
    """exa_json_path=$.type,exa_regex=({event_name}Run As Admin)""",
    """exa_json_path=$.application.file,exa_field_name=object""",
    """exa_json_path=$.elevatedApplications[0].file,exa_field_name=object""",
  ]
  ParserVersion = v1.0.0


}
```