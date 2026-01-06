#### Parser Content
```Java
{
Name = absolute-siemconnector-json-app-activity-success-catchall
  Vendor = Absolute
  Product = Absolute DDS
  ExtractionType = json
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"eventType"""", """"id"""", """"objectObjectType"""", """"objectDisplayName"""", """"actorObjectType"""" ]
  Fields = [
  	"""exa_json_path=$.createdDateTimeUtc,exa_field_name=time""",
    """exa_json_path=$.eventType,exa_field_name=operation_details""",
    """exa_json_path=$.actorObjectType,exa_field_name=object_type,exa_match_expr=!Contains($.actorObjectType,"NA")""",
    """exa_json_path=$.actorDisplayName,exa_field_name=src_host,exa_match_expr=Contains($.actorObjectType,"Device")""",
    """exa_json_path=$.actorDisplayName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),exa_match_expr=Contains($.actorObjectType,"User")""",
    """exa_json_path=$.verb,exa_field_name=operation""",
    """exa_json_path=$.objectProperties,exa_field_name=properties""",
    """exa_json_path=$.objectDisplayName,exa_field_name=object""",
    """exa_json_path=$.objectObjectType,exa_field_name=object_type"""
   ]


}
```