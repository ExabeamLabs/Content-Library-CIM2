#### Parser Content
```Java
{
Name = aws-waf-json-http-session-httprequest
  Vendor = Amazon
  Product = AWS WAF
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """"action":"""", """"httpMethod":"""", """"uri":"""", """aws:waf""", """"httpRequest":""", """"name":"user-agent"""" ]
  Fields = [
    """"timestamp":({time}\d{13}),""",
    """\s\d\d\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)""",
    """"clientIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"name":"user-agent","value":"({user_agent}[^"]+)"""",
    """"name"+:"+(?i)Host"+,"+value"+:"+({web_domain}[^="]+?({top_domain}[^\/\.\s"]+?))[\\\/\s:"]"""
    """"uri":"({uri_path}[^"]+)"""",
    """"args":"({uri_query}[^"]+)"""",
    """"action":"({action}[^"]+)"""",
    """"httpVersion":"({protocol}[^"]+)"""",
    """"httpMethod":"({method}[^"]+)"""",
    """"name":"accept","value":"({mime}[^"]+)"""",
    """"AccountName":"({aws_user}({user}[\w\.\-]{1,40}\$?))"""",
    """"webaclId":"arn:aws:waf([^:]+:){2}({account_id}\d+):"""
    """"terminatingRuleId"+:"+({rule_id}[^"]+)"""",
    """"terminatingRuleType"+:"+({rule}[^"]+)""""
    """"name"+:"+(?i)user-agent"+,"+value"+:"+(?:-|Mozilla\/[^"]+?({os}iOS|Android|BlackBerry|Windows Phone|iPhone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)[^=]+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident))"""
    """"name"+:"+(?i)Referer"+,"+value"+:"+({referrer}[^"]+)""""
  ]


}
```