#### Parser Content
```Java
{
Name = barracuda-waf-str-http-request-success-serverdefaultpassivevalid
  ParserVersion = v1.0.0
  Conditions = [ """SERVER DEFAULT PASSIVE VALID""" ]

barracuda-web-activity = {
  Vendor = Barracuda
  Product = Barracuda WAF
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+ (\+|\-)\d+)\s+(?:-|({host}\S+))\s+(\S+\s+){2}(?:-|({dest_port}\d+))\s+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+(?:-|({=src_port}\d+))\s+(\S+\s+){2}(?:-|({method}(GET|POST)))\s+(?:-|({protocol}\S+))\s+(?:-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}\S+))\s+\S+\s+(?:-|({http_response_code}\d+))\s+(?:-|({bytes_out}\d+))\s+(?:-|({bytes_in}\d+))\s+(\S+\s+){2}(?:-|({dest_translated_ip}\S+))\s+(?:-|({=dest_port}\d+))\s+(\S+\s+){5}(?:-|({action}\S+))\s+(?:-|({uri_path}\S+))\s+(?:"-"|({uri_query}[^"]+?))\s+(?:"-"|({url}[\w\-]+:\/\/\S+))\s+(?:"-"|([^"]*?))\s+"(?:-|({user_agent}[^"]+))"\s+(\S+\s+){2}(?:"-"|({user}[\w\.\-]{1,40}\$?))""",#dl field removed
    """(POST|GET)\s+\S+\s+[^\s]*?({top_domain}(?!(?:\d+\.){3}\d+)[^\.\s]+?(?:\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))+)\s""",
    """Mozilla\/[^"]+\(({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin|iPhone)[^"]+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident)""",
  
}
```