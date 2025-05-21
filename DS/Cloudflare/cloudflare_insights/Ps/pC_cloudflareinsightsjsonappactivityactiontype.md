#### Parser Content
```Java
{
Name = cloudflare-insights-json-app-activity-actiontype
  Vendor = Cloudflare
  Product = Cloudflare Insights
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """destinationServiceName =Cloudflare""" ]
  Fields = [
    """exa_json_path=$.When,exa_field_name=time"""    
    """exa_json_path=$.ActionType,exa_field_name=operation"""
    """exa_json_path=$.ActorIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..ActorEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)"""
    """exa_json_path=$.ResourceType,exa_field_name=object_type"""
    """exa_json_path=$.ActionResult,exa_field_name=result"""
    """exa_json_path=$.ResourceID,exa_field_name=object_id"""
    """exa_json_path=$..When,exa_field_name=time"""
    """exa_json_path=$..ResourceType,exa_field_name=object_type"""
    """exa_json_path=$..ActionResult,exa_field_name=result"""
    """exa_json_path=$..ResourceID,exa_field_name=object_id"""   
    """exa_json_path=$.OwnerID,exa_field_name=owner_id"""    
    """exa_regex=destinationServiceName =({app}[^\s]+)"""
    """exa_json_path=$..token_name,exa_field_name=client_token"""    
    """exa_json_path=$..ActorID,exa_field_name=user_id"""
    """exa_json_path=$.ActorID,exa_field_name=user_id"""
    """exa_json_path=$.SecurityRuleDescription,exa_field_name=additional_info"""
    """exa_json_path=$.SecurityActions,exa_field_name=action"""
    """exa_json_path=$.EdgePathingStatus,exa_field_name=status_msg"""
    """exa_json_path=$.SecurityRuleID,exa_field_name=rule_id"""
    """exa_json_path=$.EdgeResponseStatus,exa_field_name=edge_response_status"""
    """exa_json_path=$.ClientRequestHost,exa_field_name=web_domain"""
    """exa_json_path=$.EdgeResponseBytes,exa_field_name=bytes_out"""
    """exa_json_path=$.ClientRequestMethod,exa_field_name=method"""
    """exa_json_path=$.ClientRequestURI,exa_field_name=uri_path"""
    """exa_json_path=$.EdgeStartTimestamp,exa_field_name=time"""
    """exa_json_path=$.ClientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  DupFields = ["edge_response_status->http_response_code"]
}  

{
  Name = bluecatnetworks-bnetworks-json-dns-response-queryresponse
  Vendor = BlueCat Networks
  Product = BlueCat Networks
  TimeFormat = "epoch"
  ExtractionType = json
  Conditions = [ """"query":""", """"queryType":""", """"extracted_source":""", """"matchedPolicies":""", """"actionTaken":""", """"query-response"""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.actionTaken,exa_field_name=action""",
    """exa_json_path=$.query,exa_field_name=dns_query""",
    """exa_json_path=$.queryType,exa_field_name=dns_query_type""",
    """exa_json_path=$.site,exa_field_name=site_at""",
    """exa_json_path=$.response,exa_field_name=dns_response_code""",
    """exa_json_path=$.matchedPolicies[0].id,exa_field_name=policy_id""",
    """exa_json_path=$.matchedPolicies[0].name,exa_field_name=policy_name""",
    """exa_json_path=$.extracted_source,exa_field_name=src_ip"""
  ]
  ParserVersion = "v1.0.0"


}
```