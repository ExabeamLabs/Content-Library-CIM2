#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-mcasalertanubisdetection
      Vendor = Microsoft
      Product = Microsoft 365
      ExtractionType = json
      TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
      Conditions = [ """"Operation":"MCAS_ALERT_ANUBIS_DETECTION""", """"Workload"""" , """"MCAS"""", """"Microsoft""" , """"AlertSeverity"""" ]
      Fields = [
      """exa_json_path=$.AlertDisplayName,exa_field_name=alert_name"""
      """exa_json_path=$.AlertDescription,exa_field_name=alert_description"""
      """exa_json_path=$.AlertSeverity,exa_field_name=alert_severity""",
      """exa_json_path=$.AlertUri,exa_field_name=uri"""
      """exa_json_path=$.ObjectId,exa_field_name=object_id""",
      """exa_json_path=$.UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """exa_json_path=$.RecordType,exa_field_name=object_type"""
      """exa_json_path=$.CreationTime,exa_field_name=time""",
      """exa_json_path=$.Operation,exa_field_name=operation"""
      """exa_json_path=$.UserType,exa_field_name=user_type"""
      """exa_json_path=$..UserKey,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
      """exa_json_path=$.Workload,exa_field_name=app"""
      """exa_json_path=$.ResultStatus,exa_field_name=result"""
      ]
      DupFields = ["operation->event_name","operation->alert_type"]
      ParserVersion = "v1.0.0"
    

}
```