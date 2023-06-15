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
    """\d\d\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)""",
    """"clientIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"name":"user-agent","value":"({user_agent}[^"]+)"""",
    """"name":"host","value":"({web_domain}[^"]+)"""",
    """"uri":"({uri_path}[^"]+)"""",
    """"args":"({uri_query}[^"]+)"""",
    """"action":"({action}[^"]+)"""",
    """"httpVersion":"({protocol}[^"]+)"""",
    """"httpMethod":"({method}[^"]+)"""",
    """"name":"accept","value":"({mime}[^"]+)"""",
    """"AccountName":"({user}[^"]+)""""
  ]


}
```