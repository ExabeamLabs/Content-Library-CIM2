#### Parser Content
```Java
{
Name = amazon-awswaf-sk4-http-request-httprequest
  ParserVersion = v1.0.0
  Conditions = [ """"terminatingRuleType":""", """"terminatingRuleId":""", """"terminatingRuleMatchDetails":""", """httpRequest""", """maxRateAllowed"""]

aws-web-activity-event = {
    Vendor = Amazon
    Product = AWS WAF
    TimeFormat = "epoch"
    Fields = [
      """"timestamp"+:({time}\d+)""",
      """"name"+:"+(?i)Host"+,"+value"+:"+({web_domain}[^="]+?({top_domain}[^\/\.\s"]+?(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx|))+))[\\\/\s:"]""",
      """"terminatingRuleId"+:"+({rule_id}[^"]+)"""",
      """"terminatingRuleType"+:"+({rule}[^"]+)"""",
      """"action"+:"+({action}[^"]+)"""",
      """"clientIp"+:"+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
      """"httpMethod"+:"+({method}[^"]+)"""",
      """"name"+:"+(?i)Referer"+,"+value"+:"+({referrer}[^"]+)"""",
      """"name"+:"+(?i)User-Agent"+,"+value"+:"+({user_agent}[^"]+)"""",
      """"name"+:"+(?i)user-agent"+,"+value"+:"+(?:-|Mozilla\/[^"]+?({os}iOS|Android|BlackBerry|Windows Phone|iPhone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)[^=]+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident))""",
      """"uri"+:"+(/+|({uri_path}[^"]+))"""",
# http_source_id is removed
    
}
```