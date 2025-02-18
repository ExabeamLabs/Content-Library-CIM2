#### Parser Content
```Java
{
Name = beyondtrust-bi-json-app-logout-success
  Conditions = [ """"EventName":"Logout"""", """"Category":"Logout"""", """"EventSeverity":""" ]
  ParserVersion = "v1.0.0"

json-beyondtrust-beyondinsight = {
  Vendor = BeyondTrust
  Product = BeyondInsight
  ExtractionType = json
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a","M/dd/yyyy HH:mm:ss a","epoch","epoch_sec","M/d/yyyy HH:mm:ss a"] 
  Fields = [
    """exa_json_path=$..LogTime,exa_field_name=time"""
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$..EventSeverity,exa_field_name=result"""
    """exa_json_path=$..AccountName,exa_field_name=account"""
    """exa_json_path=$..SourceIp,exa_field_name=src_ip"""
    """exa_json_path=$..EventName,exa_field_name=event_name"""
    """exa_json_path=$..EventDesc,exa_field_name=event_name"""
    """exa_json_path=$..Category,exa_field_name=category"""
    """exa_json_path=$..Operation,exa_field_name=operation"""
    """exa_json_path=$..Target,exa_field_name=target"""
    """exa_json_path=$..AgentID,exa_field_name=agent_id"""
    """exa_json_path=$..Details,exa_field_name=operation_details"""
    """exa_json_path=$..RoleUsed,exa_field_name=role"""
    """exa_json_path=$..ObjectType,exa_field_name=object_type"""
    """exa_json_path=$..ObjectID,exa_field_name=object_id"""
    """exa_json_path=$..UserID,exa_field_name=user_id"""
    """exa_json_path=$..EventID,exa_field_name=event_id"""
    """exa_json_path=$..Os,exa_field_name=os"""
    """exa_json_path=$..User,exa_field_name=user"""
    """exa_json_path=$..UserName,exa_field_name=user"""
    """exa_json_path=$..AgentVer,exa_field_name=version"""
    """exa_json_path=$..ClientHost,exa_field_name=host"""
    """exa_json_path=$..SubjectDescription,exa_field_name=description"""
  
}
```