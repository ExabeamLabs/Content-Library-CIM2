#### Parser Content
```Java
{
Name = "github-g-json-app-activity-document_id"
	Vendor = "GitHub"
	Product = "GitHub"
	TimeFormat = "epoch"
	ExtractionType = json
	Conditions = [
	  """"_document_id":"""
	  """"operation_type":"""
	  """"action":"""
	]
	Fields = [
    """exa_json_path=$..@timestamp,exa_field_name=time"""
		"""exa_json_path=$.._document_id,exa_field_name=doc_id"""
		"""exa_json_path=$..token_scopes,exa_field_name=authorization_scope"""
		"""exa_json_path=$..programmatic_access_type,exa_field_name=access_type"""
		"""exa_json_path=$..user,exa_field_name=user"""
		"""exa_json_path=$..user_agent,exa_field_name=user_agent"""
		"""exa_json_path=$..user_id,exa_field_name=user_id"""
		"""exa_json_path=$..operation_type,exa_field_name=operation_type"""
		"""exa_json_path=$..business,exa_field_name=company"""
		"""exa_json_path=$.action,exa_field_name=action"""
    """exa_json_path=$.attributes.action,exa_field_name=action"""
    """exa_json_path=$..email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)"""
		"""exa_json_path=$..external_identity_username,exa_field_name=user_ou"""
		"""exa_json_path=$..actor_location.country_code,exa_field_name=country_code"""
		"""exa_json_path=$..external_identity_username,exa_field_name=additional_info"""
	]
	ParserVersion = "v1.0.0"


}
```