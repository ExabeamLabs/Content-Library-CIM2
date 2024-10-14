#### Parser Content
```Java
{
Name = "mvision-m-json-alert-trigger-success-outgoingmemoryviacloud"
Conditions = [
""""threattype":"""
"""OUTGOING_MEMORY_VIA_CLOUD"""
""""PolicyName":"""
""""threatseverity":"""
]
ParserVersion = "v1.0.0"

Mvision-json-template = {
    Vendor = "Mvision"
    Product = "Mvision"
    TimeFormat = "epoch"
    ExtractionType = json
    Fields = [
      """"detectedutc\":\s*\"({time}\d{13})\""""
      """"analyzerhostname\":\s*\"({host}[^\"]+)\""""
      """"UserPrincipalName\":\s+\"(({email_address}[^@\"]+@[^.\"]+\.[^\"]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\"]+))|({=user}[^\"]+))\""""
      """"SourceUsername\":\s*\"(({domain}[^\\\"]+)\\\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
      """"sourceipv4\":\s*\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
      """"targetipv4\":\s*\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
      """"threattype\":\s*\"({alert_name}[^\"]+)\""""
      """"threatseverity\":\s*\"({alert_severity}\d+)\""""
      """"threateventid\":\s*({alert_id}\d+)"""
      """"PolicyName\":\s*\"({alert_type}[^\"]+)\""""
      """"TotalContentSize\":\s*({bytes}\d+)"""
      """"targetfilename\":\s*\"({target}[^\"]+)\""""
      """"threatactiontaken\":\s*\"({action}[^\"]+)\""""
      """"RuleNames\":\s+\"({rule}[^\"]+)\""""
      """"EmailSubject\":\s*\"({alert_subject}[^\"]+)\""""
      """"MatchedEmailRecipients\":\s*\"({email_recipients}[^\"]+?)\s*\""""
      """"EmailSender\":\s*\"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\""""
      """"PrinterName\":\s*\"({printer_name}[^\"]+)\""""
      """"Destination\":\s+\"({target}[^\"]+)\""""
      """"ActualURL\":\s*\"(_NOT_AVAILABLE_|({url}[^\"]+))\""""
      """"DisplayName\":\s+\"({additional_info}[^\"]+)\""""
      """"targetprocessname\":\s*\"({process_name}[^\"]+)\""""
      """exa_json_path=$.detectedutc,exa_field_name=time""",
      """exa_json_path=$.analyzerhostname,exa_field_name=host""",
      """exa_json_path=$.UserPrincipalName,exa_regex=(({email_address}[^@\"]+@[^.\"]+\.[^\"]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\"]+))|({=user}[^\"]+))\""""
      """exa_regex="SourceUsername\":\s*\"(({domain}[^\\\"]+)\\\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
      """exa_json_path=$.sourceipv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
      """exa_json_path=$.targetipv4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
      """exa_json_path=$.threattype,exa_field_name=alert_name"""
      """exa_json_path=$.threatseverity,exa_field_name=alert_severity"""
      """exa_json_path=$.threateventid,exa_field_name=alert_id"""
      """exa_json_path=$.PolicyName,exa_field_name=alert_type"""
      """exa_json_path=$.TotalContentSize,exa_field_name=bytes"""
      """exa_json_path=$.targetfilename,exa_field_name=target"""
      """exa_json_path=$.threatactiontaken,exa_field_name=action"""
      """exa_json_path=$.RuleNames,exa_field_name=rule"""
      """exa_json_path=$.EmailSubject,exa_field_name=alert_subject"""
      """exa_json_path=$.MatchedEmailRecipients,exa_field_name=recipients"""
      """exa_regex="EmailSender\":\s*\"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\""""
      """exa_json_path=$.PrinterName,exa_field_name=printer_name"""
      """exa_json_path=$.Destination,exa_field_name=target"""
      """exa_json_path=$.ActualURL,exa_field_name=url,exa_match_expr=!InList($.ActualURL,"_NOT_AVAILABLE_")"""
      """exa_json_path=$.DisplayName,exa_field_name=additional_info"""
      """exa_json_path=$.targetprocessname,exa_field_name=process_name"""
      
}
```