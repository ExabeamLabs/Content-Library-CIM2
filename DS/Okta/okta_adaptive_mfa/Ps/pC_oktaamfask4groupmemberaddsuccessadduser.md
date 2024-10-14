#### Parser Content
```Java
{
Name = okta-amfa-sk4-group-member-add-success-adduser
  Vendor = Okta
  Product = Okta Adaptive MFA
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"eventType":"group.user_membership.add"""", """"Add user to group membership"""", """"actor":""", """"alternateId":"""" ]
  Fields=[
    """"published":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
    """"actor":\{[^\}]*?("type":"User",)?"alternateId":"((({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|unknown|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"actor":\{[^\}]*?("type":"User"[^\}]*?)?"displayName":"(Okta System|({full_name}({first_name}[^"]+?)\s({last_name}[^"\s]+)))"""",
    """"type":"User".*?"displayName":"({group_name}[^"]+)".*?"id":"({group_id}[^"]+)".*?"type":"UserGroup"""",
    """\{"id":"({group_id}[^"]+)","type":"UserGroup"[^\}]*?"displayName":"({group_name}[^"]+)"""",
    """"target":\[[^\]]*?("type":"User",)?"alternateId":"({account_id}[^"]+)"""",
    """"target":\[[^\]]*?("type":"User",)?"alternateId":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|unknown|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"ipAddress":"?(null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),?"?""",
    """"outcome":\{"result":"({result}[^"]+)"""",
    """duser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*""",
    """"target(s)?":[^\]]+?"displayName":"({member}[^",]+)[^\]\}]+?("type":"User")?"""
    """"eventType":\s*"({operation}[^"]+)""""
    """"legacyEventType":\s*"({operation_details}[^"]+)""""
    """outcome":[^\]]*?"result":"?(null|({result}[^\"]+))"?,"reason":"?(null|({result_reason}[^"]+))""",
    """"debugData":.*?"risk":\s*"[^"]*?level=({severity}[^"\}]+)("|\})"""
    """"os":\s*"({os}[^"]+)""""
    """"displayMessage"\s*:\s*"((?i)null|({event_name}[^",]+))"""
    """exa_json_path=$.published,exa_field_name=time""",
    """exa_json_path=$.target[1:].alternateId,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),exa_match_expr=Contains($.target.type,"User")""",
    """exa_json_path=$..client.ipAddress,exa_regex=(null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """exa_json_path=$..outcome.result,exa_field_name=result""",
    """exa_json_path=$..target[1:].displayName,exa_field_name=member,exa_match_expr=Contains($.target.type,"User")""",
    """exa_json_path=$..eventType,exa_field_name=operation""",
    """exa_json_path=$..legacyEventType,exa_field_name=operation_details,exa_match_expr=!Contains($.legacyEventType,"null")""",
    """exa_regex="outcome":[^\]]*?"result":"?(null|({result}[^\"]+))"?,"reason":"?(null|({result_reason}[^"]+))""",
    """exa_json_path=$..debugContext.debugData.risk,exa_regex=^[^"]*?level=({severity}[^"\}]+)("|\})""",
    """exa_json_path=$..client.userAgent.os,exa_field_name=os""",
    """exa_json_path=$..displayMessage,exa_field_name=event_name"""
    """exa_regex="actor":\{[^\}]*?("type":"User",)?"alternateId":"((({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|unknown|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """exa_regex="actor":\{[^\}]*?("type":"User"[^\}]*?)?"displayName":"(Okta System|({full_name}({first_name}[^"]+?)\s({last_name}[^"\s]+)))"""",
    """exa_regex="type":"User".*?"displayName":"({group_name}[^"]+)".*?"id":"({group_id}[^"]+)".*?"type":"UserGroup"""",
    """exa_regex=\{"id":"({group_id}[^"]+)","type":"UserGroup"[^\}]*?"displayName":"({group_name}[^"]+)"""",
    """exa_json_path=$.target[?(@.type == 'User')].alternateId,exa_field_name=account_id""",
    """exa_json_path=$.target[?(@.type == 'User')].alternateId,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|unknown|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.target[?(@.type == 'User')].displayName,exa_field_name=member"""
  ]
  DupFields = [ "dest_user->account_name" ]
  ParserVersion = "v1.0.0"


}
```