#### Parser Content
```Java
{
Name = mcafee-wg-str-http-session-denied
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Web Gateway
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ ""","DENIED",""" , ""","http""" ]
  Fields = [
  """^(?:\\"|"{4}|"{2}|").*?(?:\\"|")*,(?:\\"|"{4}|"{2}|")({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\"|")*,""",
 ""","DENIED",("(|[^"]+)",){18}"({dest_port}\d+)"""",
 ""","DENIED",("(|[^"]+)",){17}"({dest_ip}[a-fA-F\d:.]+)"""",
 ""","DENIED",("(|[^"]+)",){15}"[^"]+?\(({os}iOS|Android|BlackBerry|iPhone OS|Windows Phone|BeOS|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)""",
 ""","DENIED",("(|[^"]+)",){15}"({user_agent}[^"]+?)\s*"""",
 ""","DENIED",("(|[^"]+)",){13}"({browser}[^"]+)"""",
 ""","DENIED",("(|[^"]+)",){12}"({failure_reason}[^"]+)"""",
 ""","DENIED",("(|[^"]+)",){9}"({http_response_code}\d+)"""",
 ""","DENIED",("(|[^"]+)",){8}"({rule}[^"]+)"""",
 ""","DENIED",("(|[^"]+)",){5}"({mime}[^"]+)"""",
 ""","DENIED",("(|[^"]+)",){4}"({categories}({category}[^,"]+)[^"]*)"""",
 ""","DENIED",("(|[^"]+)",){3}"({protocol}[^"]+)"""",
 ""","DENIED",("(|[^"]+)",){2}"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
 """({action}DENIED)""",
 ""","({uri_path}[^"]+)","DENIED"""",
 ""","[^"]*?({top_domain}(?!(?:\d+\.){3}\d+)[^\.\s;"]+(?:\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch|local|th|goog|link|ai|tech|network|ms|ly))+)","[^"]+","DENIED"""",
 ""","((\d{1,3}\.){3}\d{1,3}|({web_domain}[^"]+))",("[^"]+",)"DENIED"""",
 ""","({bytes_out}\d+)",("[^"]+",){2}"DENIED"""",
 ""","({bytes_in}\d+)",("[^"]+",){3}"DENIED"""",
 ""","({method}[^"]+)",("[^"]+",){4}"DENIED"""",
 ""","({src_ip}[a-fA-F\d:.]+)",("[^"]+",){5}"DENIED"""",
 ""","({domain}[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)",("[^"]+",){6}"DENIED""""
 ]

 

}
```