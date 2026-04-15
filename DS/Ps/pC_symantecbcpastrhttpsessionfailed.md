#### Parser Content
```Java
{
Name = "symantec-bcpa-str-http-session-failed"
  ParserVersion = "v1.0.0"
  Conditions = [ """PROXIED""", """ ssl """]

bluecoat-proxy}{
  Name = "symantec-bcpa-mix-http-session-ssldenied"
  ParserVersion = "v1.0.0"
  Conditions = [
    """ DENIED """
    """ ssl """
  ]
  Fields = ${BlueCoatParserTemplates.bluecoat-proxy.Fields}[
    """\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s([^\s]+\s){3}({action}OBSERVED|PROXIED|DENIED)""",
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\dZ)\s+({host}[\w\-.]+)\s+[\w+\s+\d+]+\s+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s+[\-\w+\d+]+\s+(-|"?[^"]*")\s+({method}[^\s]+)\s+({protocol}[^\s]+)\s+""",
    """\s+({action}OBSERVED|PROXIED|DENIED)\s+"*({category}[^"]+)"*\s*(?:-|\\?"(none|({categories}[^\\";]+[^"]*?))\\?")\s+(?:-|({proxy_action}[^\s]+))\s+(?:-|({referrer}[^\s]+))\s+(?:-|({http_response_code}\d+)?)\s+[^"]+"({method}[^"]+)"(\s+[\w\-\.\/]+){6}(\s+|")({user_agent}[^\%\s]+)\s*"""
  
}
```