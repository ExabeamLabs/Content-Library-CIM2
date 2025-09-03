#### Parser Content
```Java
{
Name = halcyon-halcyon-json-alert-trigger-success-alert
    Vendor = Halcyon
    Product = Halcyon
    ParserVersion = v1.0.0
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
    Conditions = [ """"dataType":"Alert"""", """"kind":""", """"action":""", """"summary":""", """"artifact":""" ]
    Fields = [
      """exa_json_path=$.kind,exa_field_name=alert_name"""
      """exa_json_path=$.lastOccurredAt,exa_field_name=time"""
      """exa_json_path=$.action,exa_field_name=action"""
      """exa_json_path=$.primaryProcess.commandLine,exa_field_name=process_command_line"""
      """exa_json_path=$.summary.artifact.filePath,exa_field_name=file_path"""
      """exa_json_path=$.summary.artifact.sha256,exa_field_name=hash_sha256"""
    ]
    DupFields = [ "alert_name->alert_type", "alert_name->alert_subject"]


}
```