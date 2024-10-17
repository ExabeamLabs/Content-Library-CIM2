#### Parser Content
```Java
{
Name = amazon-awswaf-json-app-authentication-httprequest
  ParserVersion = v1.0.0
  Conditions = [ """"terminatingRuleType"""", """"terminatingRuleId"""", """"terminatingRuleMatchDetails"""", """httpRequest""", """":"""" ]

aws-web-activity-event = {
    Vendor = Amazon
    Product = AWS WAF
    ExtractionType = json
    TimeFormat = "epoch"
    Fields = [
      """"timestamp"+:({time}\d{13})""",
      """"name"+:"+(?i)Host"+,"+value"+:"+({web_domain}[^="]+?({top_domain}[^\/\.\s"]+?(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx|))+))[\\\/\s:"]""",
      """"terminatingRuleId"+:"+({rule_id}[^"]+)"""",
      """"terminatingRuleType"+:"+({rule}[^"]+)"""",
      """"action"+:"+({action}[^"]+)"""",
      """"clientIp"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"httpMethod"+:"+({method}[^"]+)"""",
      """"name"+:"+(?i)Referer"+,"+value"+:"+({referrer}[^"]+)"""",
      """"name"+:"+(?i)User-Agent"+,"+value"+:"+({user_agent}[^"]+)"""",
      """"name"+:"+(?i)user-agent"+,"+value"+:"+(?:-|Mozilla\/[^"]+?({os}iOS|Android|BlackBerry|Windows Phone|iPhone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)[^=]+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident))""",
      """"uri"+:"+(/+|({uri_path}[^"]+))"""",
      """"responseCodeSent":"?(null|({http_response_code}\d+))""",
      """"webaclId":"arn:aws:waf([^:]+:){2}({account_id}\d+):""",
      """"account"+:"+({aws_account}[^"]+)"""",
      """exa_json_path=$.timestamp,exa_field_name=time""",
      """exa_json_path=$.terminatingRuleId,exa_field_name=rule_id""",
      """exa_json_path=$.terminatingRuleType,exa_field_name=rule""",
      """exa_json_path=$.action,exa_field_name=action""",
      """exa_json_path=$.httpMethod,exa_field_name=method""",
      """exa_json_path=$.uri,exa_field_name=uri_path""",
      """exa_json_path=$.responseCodeSent,exa_field_name=http_response_code""",
      """exa_json_path=$.webaclId,exa_regex=arn:aws:waf([^:]+:){2}({account_id}\d+):""",
      """exa_json_path=$.httpRequest.clientIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$.httpRequest.headers[?(@.name == 'Host')].value,exa_regex=({web_domain}[^="]+?({top_domain}[^\/\.\s"]+?(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx|))+))[\\\/\s:"]""",
      """exa_json_path=$.httpRequest.headers[*].value,exa_field_name=user_agent,exa_match_expr=Contains(toLower($.httpRequest.headers[*].name),"referer")"""
      """exa_json_path=$.httpRequest.headers[*].value,exa_field_name=user_agent,exa_match_expr=Contains(toLower($.httpRequest.headers[*].name),"user-agent")"""
      """exa_json_path=$.account,exa_field_name=aws_account""",
# http_source_id is removed
    
}
```