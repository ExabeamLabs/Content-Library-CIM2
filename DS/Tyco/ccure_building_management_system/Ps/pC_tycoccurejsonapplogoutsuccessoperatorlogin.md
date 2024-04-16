#### Parser Content
```Java
{
Name = tyco-ccure-json-app-logout-success-operatorlogin
  ExtractionType = json
  Vendor = Tyco
  Product = CCURE Building Management System
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"messagetype":"OperatorLogin"""", """"statecode":"LoggedOut"""", """"primaryobjectname":"""" ]
  Fields = [
    """exa_json_path=$.messageutc,exa_field_name=time"""
    """exa_json_path=$.statecode,exa_field_name=event_name"""
    """exa_json_path=$.primaryobjectname,exa_regex=({last_name}[^\s]+?)\s+({first_name}[^",\s]+)"""
    """exa_json_path=$.xmlmessage,exa_regex=<ApplicationName[^>]*>({app}[^<"]+)<\/ApplicationName>"""
  ]


}
```