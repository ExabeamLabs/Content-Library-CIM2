#### Parser Content
```Java
{
Name = microsoft-sentinel-json-process-create-success-processcreation
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Microsoft Sentinel
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Conditions = [ """"Type":"BehaviorAnalytics"""", """"ActivityType":"ProcessTracking"""", """"ActionType":"Process Creation"""" ]
    Fields=[
      """exa_json_path=$.TimeGenerated,exa_field_name=time"""
      """exa_json_path=$.ActivityInsights.CommandLine,exa_field_name=process_command_line"""
      """exa_json_path=$.ActivityInsights.ParentProcessName,exa_regex=(|({parent_process_path}({parent_process_dir}[^"]*?)(\\+({parent_process_name}[^"\\]+?))?))"""
      """exa_json_path=$.ActivityInsights.NewProcessId,exa_field_name=process_id"""
      """exa_json_path=$.ActivityInsights.Process,exa_field_name=process_name"""
      """exa_json_path=$.ActivityInsights.NewProcessName,exa_regex=(|({process_path}({process_dir}[^"]*?)(\\+({process_name}[^"\\]+?))?))"""
      """exa_json_path=$.ActivityInsights.ProcessId,exa_field_name=parent_process_id"""
      """exa_json_path=$.UserName,exa_field_name=user"""
      """exa_json_path=$.UsersInsights.AccountDomain,exa_field_name=domain"""
      """exa_json_path=$.TenantId,exa_field_name=tenant_id"""
      """exa_json_path=$.SourceDevice,exa_field_name=host"""
      """exa_json_path=$.ActivityInsights.MandatoryLabel,exa_field_name=user_sid"""
      """exa_regex="ParentProcessName":"(|({parent_process_path}({parent_process_dir}[^"]*?)(\\+({parent_process_name}[^"\\]+?))?))""""
      """exa_regex="NewProcessName":"(|({process_path}({process_dir}[^"]*?)(\\+({process_name}[^"\\]+?))?))""""
    ]


}
```