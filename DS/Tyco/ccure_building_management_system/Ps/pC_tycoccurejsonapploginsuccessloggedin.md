#### Parser Content
```Java
{
Name = "tyco-ccure-json-app-login-success-loggedin"
ExtractionType = json
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""messagetype":""""
""""statecode":"LoggedIn""""
""""primaryobjectname":""""
]
Fields = [
  """exa_json_path=$.messageutc,exa_field_name=time"""
  """exa_json_path=$.statecode,exa_field_name=event_name"""
  """exa_json_path=$.primaryobjectname,exa_regex=({last_name}[^"\s,]+?)\s+({first_name}[^",]+)"""
  """exa_json_path=$.xmlmessage,exa_regex=<ApplicationName[^>]*>({app}[^<"]+)<\/ApplicationName>"""

]
ParserVersion = "v1.0.0"


}
```