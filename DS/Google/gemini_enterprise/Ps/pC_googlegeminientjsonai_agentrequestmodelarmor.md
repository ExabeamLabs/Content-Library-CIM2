#### Parser Content
```Java
{
Name = google-geminient-json-ai_agent-request-modelarmor
  ExtractionType = json
  Vendor = Google
  Product = Gemini Enterprise
  ParserVersion = "v1.0.0"
  TimeFormat = [ """yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ""" ]
  Conditions = [ """modelarmor.googleapis.com""" ]
  Fields = [
    """exa_json_path=$..sanitizationResult..sanitizationVerdict,exa_regex=\w+({result}(?i)ALLOW|BLOCK)""",
    """exa_json_path=$..sanitizationResult..sanitizationVerdictReason,exa_field_name=result_reason"""
    """exa_json_path=$..sanitizationResult..sanitizationVerdictReason,exa_regex=({result_reason}[^"]+)"""
    """exa_json_path=$..operationType,exa_field_name=event_name"""
    """exa_json_path=$.severity,exa_field_name=severity"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$..sanitizationMetadata.errorCode,exa_field_name=failure_code"""
    """exa_json_path=$..sanitizationMetadata.errorMessage,exa_field_name=failure_reason"""
    """exa_json_path=$..filterResults,exa_field_name=additional_info"""
    """exa_json_path=$.labels.['modelarmor.googleapis.com/client_correlation_id'],exa_regex=[^,"]+default_assistant\|({identifier}[^",]+)"""
    """exa_json_path=$.labels.['modelarmor.googleapis.com/client_name'],exa_field_name=client_name"""
  ]


}
```