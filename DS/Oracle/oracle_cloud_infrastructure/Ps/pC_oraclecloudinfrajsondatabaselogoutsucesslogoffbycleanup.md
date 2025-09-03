#### Parser Content
```Java
{
Name = oracle-cloudinfra-json-database-logout-sucess-logoffbycleanup
  ParserVersion = "v1.0.0"
  Conditions = [ """"ddsource":"oracle_cloud"""",""""source":"OracleDatabaseUnifiedAudit"""",""""eventName":"LOGOFF BY CLEANUP"""" ]

oracle-cloudinfra-db-events = {
    Vendor = Oracle
    Product = Oracle Cloud Infrastructure
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Fields = [
          """exa_json_path=$..auditEventTime,exa_field_name=time"""
          """exa_json_path=$..dbUserName,exa_field_name=db_user"""
          """exa_json_path=$..clientHostname,exa_field_name=src_host"""
          """exa_json_path=$..clientIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
          """exa_json_path=$..eventName,exa_field_name=event_name""",
          """exa_json_path=$..operationStatus,exa_field_name=result""",
          """exa_json_path=$..operation,exa_field_name=operation""",
          """exa_json_path=$..osUserName,exa_field_name=user""",
          """exa_json_path=$..clientProgram,exa_field_name=app""",
          """exa_json_path=$..databaseUniqueName,exa_field_name=db_name"""
          """exa_json_path=$..commandText,exa_field_name=db_query"""
    
}
```