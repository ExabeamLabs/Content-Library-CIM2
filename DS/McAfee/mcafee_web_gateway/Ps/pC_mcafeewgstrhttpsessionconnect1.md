#### Parser Content
```Java
{
Name = mcafee-wg-str-http-session-connect-1
    ParserVersion = v1.0.0
    Conditions = [ ""","OBSERVED",""", ""","http""" ]
    Vendor = McAfee
    Product = McAfee Web Gateway
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd HH:mm:ss"]
    Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s({host}[\w\-.]+)\s(\S+\s+){4}"({user}[\w\.\-\!\#\^\~]{1,40}\$?)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({method}[^"]+)","({bytes_in}\d+)","({bytes_out}\d+)","(({url}[^?";]+)","({uri_path}\/[^\s\?]*)?)","({action}OBSERVED|PROXIED|DENIED)",("[^"]*",){3}"({protocol}[^"]+)","({categories}({category}[^,"]+?)(,[^"]*)?)",("[^"]*",){4}"({http_response_code}\d+)","({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",("[^"]*",){2}"({browser}[^"]+)","[^"]*","(\s*|({user_agent}[^"]+))""""
    """"({user}[\w\.\-\!\#\^\~]{1,40}\$?)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({method}[^"]+)","({bytes_in}\d+)","({bytes_out}\d+)","(({url}[^?";]+)","({uri_path}\/[^\s\?]*)?)","({action}OBSERVED|PROXIED|DENIED)",([^,]+,){2}"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)","({protocol}[^"]+)","({categories}({category}[^,"]+?)(,[^"]*)?)",("[^"]*",){4}"({http_response_code}\d+)","({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",("[^"]*",){2}"({browser}[^"]+)","[^"]*","(\s*|({user_agent}[^"]+))""""

 ""","({domain}[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)",("[^"]+",){6}"OBSERVED"""",
 ""","({src_ip}[a-fA-F\d:.]+)",("[^"]+",){5}"OBSERVED"""",
 ""","({method}[^"]+)",("[^"]+",){4}"OBSERVED"""",
 ""","({bytes_in}\d+)",("[^"]+",){3}"OBSERVED"""",
 ""","({bytes_out}\d+)",("[^"]+",){2}"OBSERVED"""",
 ""","((\d{1,3}\.){3}\d{1,3}|({web_domain}[^"]+))",("[^"]+",)"OBSERVED"""",
 ""","[^"]*?({top_domain}(?!(?:\d+\.){3}\d+)[^\.\s;"]+(?:\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch|local|th|goog|link|ai|tech|network|ms|ly))+)","[^"]+","OBSERVED"""",
 ""","({uri_path}[^"]+)","OBSERVED"""",
 """({action}OBSERVED)""",
 ""","OBSERVED",("(|[^"]+)",){2}"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
 ""","OBSERVED",("(|[^"]+)",){3}"({protocol}[^"]+)"""",
 ""","OBSERVED",("(|[^"]+)",){4}"({categories}({category}[^,"]+)[^"]*)"""",
 ""","OBSERVED",("(|[^"]+)",){5}"({mime}[^"]+)"""",
 ""","OBSERVED",("(|[^"]+)",){8}"({rule}[^"]+)"""",
 ""","OBSERVED",("(|[^"]+)",){9}"({http_response_code}\d+)"""",
 ""","OBSERVED",("(|[^"]+)",){12}"({failure_reason}[^"]+)"""",
 ""","OBSERVED",("(|[^"]+)",){13}"({browser}[^"]+)"""",
 ""","OBSERVED",("(|[^"]+)",){15}"({user_agent}[^"]+?)\s*"""",
 ""","OBSERVED",("(|[^"]+)",){15}"[^"]+?\(({os}iOS|Android|BlackBerry|iPhone OS|Windows Phone|BeOS|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)""",
 ""","OBSERVED",("(|[^"]+)",){17}"({dest_ip}[a-fA-F\d:.]+)"""",
 ""","OBSERVED",("(|[^"]+)",){18}"({dest_port}\d+)"""",
 """^(?:\\"|"{4}|"{2}|").*?(?:\\"|")*,(?:\\"|"{4}|"{2}|")({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\"|")*,"""
    ]


}
```