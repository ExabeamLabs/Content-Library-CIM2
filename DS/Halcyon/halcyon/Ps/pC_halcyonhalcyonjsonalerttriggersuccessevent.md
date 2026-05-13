#### Parser Content
```Java
{
Name = halcyon-halcyon-json-alert-trigger-success-event
    Vendor = Halcyon
    Product = Halcyon
    ParserVersion = v1.0.0
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
    Conditions = [ """"dataType":"Event"""", """"kind":""", """"action":""", """"id":""", """"artifact":""" ]
    Fields = [
      """exa_json_path=$.kind,exa_field_name=alert_name"""
      """exa_json_path=$.kind,exa_field_name=alert_type"""
      """exa_json_path=$.kind,exa_field_name=alert_subject"""
      """exa_json_path=$.reason.exitCode,exa_field_name=alert_reason"""
      """exa_json_path=$.occurredAt,exa_field_name=time"""
      """exa_json_path=$.action,exa_field_name=action"""
      """exa_json_path=$.asset.id,exa_field_name=asset_id"""
      """exa_json_path=$.asset.name,exa_field_name=host"""
      """exa_json_path=$.tenantId,exa_field_name=tenant_id"""
      """exa_json_path=$.process.commandLine,exa_field_name=process_command_line"""
      """exa_json_path=$.process.artifact.filePath,exa_regex=({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))"""
      """exa_json_path=$.summary.artifact.filePath,exa_regex=({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))"""
      """exa_json_path=$.summary.artifact.sha256,exa_field_name=hash_sha256"""
      """exa_json_path=$.summary.applicationName,exa_field_name=app"""
      """exa_json_path=$.kind,exa_field_name=event_name"""
      """exa_json_path=$.kind,exa_field_name=operation"""
      """exa_json_path=$.primaryProcess.pid,exa_field_name=process_id"""
      """exa_json_path=$.primaryProcess.parentPid,exa_field_name=parent_process_id"""
    ]


}
```