#### Parser Content
```Java
{
Name = tyco-ccure-json-physical-location-modify-success-objectchangedstate
  ExtractionType = json
  Vendor = Tyco
  Product = CCURE Building Management System
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"messagetype":"ObjectChangedState"""", """"statecode":"""", """"primaryobjectname":"""" ]
  Fields = [
    """exa_json_path=$.messageutc,exa_field_name=time"""
    """exa_json_path=$.statecode,exa_field_name=operation"""
    """exa_json_path=$.messagetype,exa_field_name=result"""
    """exa_json_path=$.primaryobjectname,exa_field_name=object"""
    """exa_json_path=$.primaryobjecttype,exa_field_name=object_type"""
  ]


}
```