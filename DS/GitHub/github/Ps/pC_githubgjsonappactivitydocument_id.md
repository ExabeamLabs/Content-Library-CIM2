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
        """exa_json_path=$.external_identity_username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
        """exa_json_path=$.external_identity_username,exa_regex=^[^@"]+?@({domain}[^"]+)$"""

        """"@timestamp":({time}\d{13}),""",
        """({host}\S+)\s+github_audit:""",
        """"_document_id":\s*"({doc_id}[^"]+)"""",
        """"user":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
        """"user_agent":\s*"({user_agent}[^"]+)"""",
        """"user_id":\s*({user_id}\d+)""",
        """"operation_type":\s*"({operation_type}[^"]+)"""",
        """"business":\s*"({company}[^"]+)"""",
        """"action":\s*"({action}[^"]+)"""",
        """"email":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)"""",
        """"country_code":\s*"({country_code}[^"]+)"""",
        """"actor_ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
	]
	ParserVersion = "v1.0.0"


}
```