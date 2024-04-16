#### Parser Content
```Java
{
Name = "okta-amfa-sk4-group-member-remove-success-groupmembership"
  Vendor = Okta
  Product = Okta Adaptive MFA
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"eventType":"group.user_membership.remove"""", """"actor":""", """"type":""", """"legacyEventType":"core.user_group_member.user_remove"""" ]
  Fields = [
    """"published":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"actor":\{[^\}]+?"type":"User","alternateId":"((({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""",
    """"actor":\{[^\}]+?"type":"User"[^\}]+?"displayName":"({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))"""",
    """"target":\[[^\]]+?"type":"+User","alternateId":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?))"""",
    """"target":\[[^\]]+?"type":"({object_type}[^"]+)"""",
    """"type":"UserGroup"[^\}]+?"displayName":"({group_name}[^"]+)"""",
    """displayMessage":"({event_name}[^"]+)"""",
    """"eventType":"({operation_details}({event_code}[^"]+))"""",
    """"result":"({result}[^"]t+)""""
    """"legacyEventType":\s*"({operation}[^"]+)""""
    """outcome":[^\]]*?"result":"?(null|({outcome_result_at}[^\"]+))"?,"reason":"?(null|({outcome_reason_at}[^"]+))"""
    """"debugData":.*?"risk":\s*"[^"]*?level=({severity}[^"\}]+)("|\})"""
    """"os":\s*"({os}[^"]+)""""
    """exa_json_path=$.published,exa_field_name=time""",
    """exa_json_path=$.client.ipAddress,exa_regex=(null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """exa_json_path=$.actor.alternateId,exa_regex=((({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-]{1,40}\$?)),exa_match_expr=Contains($.actor.type,"User")""",
    """exa_json_path=$.actor.displayName,exa_regex=(Okta System|({full_name}({first_name}[^"]+?)\s({last_name}[^"\s]+))),exa_match_expr=Contains($.actor.type,"User")""",
    """exa_json_path=$.target[1:].displayName,exa_field_name=group_name,exa_match_expr=Contains($.target.type,"UserGroup")""",
    """exa_json_path=$.target[1:].id,exa_field_name=group_id,exa_match_expr=Contains($.target.type,"UserGroup")""",
    """exa_json_path=$.target[1:].alternateId,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?)),exa_match_expr=Contains($.target.type,"User")""",
    """exa_regex="target":\[[^\]]+?"type":"({object_type}[^"]+)"""",    """exa_json_path=$.displayMessage,exa_field_name=event_name"""
    """exa_json_path=$.eventType,exa_field_name=operation_details""",
    """exa_json_path=$.eventType,exa_field_name=event_code""",
    """exa_json_path=$.legacyEventType,exa_field_name=operation,exa_match_expr=!Contains($.legacyEventType,"null")""",
    """exa_json_path=$.outcome.result,exa_field_name=result""",
    """exa_regex=outcome":[^\]]*?"result":"?(null|({outcome_result_at}[^\"]+))"?,"reason":"?(null|({outcome_reason_at}[^"]+))"""
    """exa_json_path=$.debugContext.debugData.risk,exa_regex=^[^"]*?level=({severity}[^"\}]+)("|\})""",
    """exa_json_path=$.client.userAgent.os,exa_field_name=os"""
  ]
  DupFields = [ "dest_user->account_name" ]
  ParserVersion = "v1.0.0"


}
```