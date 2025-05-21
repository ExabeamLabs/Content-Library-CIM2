#### Parser Content
```Java
{
Name = mcafee-wg-kv-http-session-fail-mwg
  Vendor = Skyhigh Security
  Product = Secure Web Gateway
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """ mwg:""", """ McAfeeWG:Error|""", """|action_name=""", """|http_method=""" ]
  Fields = [
    """\|date=\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d\s[+-]\d+)\]\|""",
    """\|system_hostname=({host}[\w\-.]+)\|""",
    """\|user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\|""",
    """\|Error_ID=({failure_code}\d+)\|""",
    """\|Error_descr=({failure_reason}[^\|]+)\|""",
    """\|action_name=({action}[^\|]+)\|""",
    """\|src_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|""",
    """\|dest_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\|""",
    """\|dest_host=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[^\|]+))\|""",
    """\|dest_port=({dest_port}\d+)\|""",
    """\|status=({http_response_code}\d+)\|""",
    """\|http_method=({method}[^\|]+)\|""",
    """\|http_user_agent=({user_agent}[^\|]+)\|""",
    """\|http_referrer=({referrer}[^\|]+)\|""",
    """\|url=({url}[^\|]+)\|""",
    """\|file_hash=({file_hash}[^\|]+)\|""",
    """\|file_name=({file_name}[^\|]+)\|"""
  ]
  ParserVersion = "v1.0.0"


}
```