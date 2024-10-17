#### Parser Content
```Java
{
Name = mcafee-wg-str-http-session-post
  ParserVersion = v1.0.0
  Conditions = [ """"Vendor:McAfee""","""POST """ ]

mcafee-http-session-1 = {
    Vendor = McAfee
    Product = McAfee Web Gateway
    TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
    Fields = [
	"""\[({time}\d\d\/\w\w\w\/\d\d\d\d:\d\d:\d\d:\d\d\s[+-]\d+)\]\s\\?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?"\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s(|({http_response_code}\d+))\s\\?"(|({method}\S+))\s(|({url}(\w+:\/+)?[^;\s\/]*?((?!(?:\d+\.){3}\d+)[^\.\s;\s]+(?:\.)+)?(:({=dest_port}\d+))?({uri_path}\/[^;\s\?]*?)?({uri_query}\?[^;\s]*?)?))\s(|({protocol}[^"\\]+))\\?"\s\\?"(|({categories}({category}[^,"\\]+)[^"\\]*))\\?"\s\\?"[^"]+"\s\\"(|({mime}[^"\\]+))\\?"\s(|(\d+))\s\\?"(|({user_agent}[^\\"]+))\\?"\s\S+\s\\?""""
	
}
```