#### Parser Content
```Java
{
Name = mcafee-wg-csv-http-session-3
    ParserVersion = "v1.0.0"
    Vendor = Skyhigh Security
    Product = Secure Web Gateway
    TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
    Conditions = [ """mwg: [""", """);""" ]
    Fields = [
        """mwg: \[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [\+\-]\d+)\]\s*"(|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*({http_response_code}\d+)\s*"({method}\S+)\s({url}({protocol}\w+:\/\/)?({web_domain}[^\s\/\?"]+)({uri_path}\/[^\s"\?]*))(\?({uri_query}[^"\s]+))?\s*[^"]+"\s*"({categories}({category}[^",]+)[^"]*)"\s"[^"]+"\s"({mime}[^"]+)"\s*({bytes_in}\d+)\s*"({user_agent}[^"]+)"\s*("[^"]*"\s*){2}({bytes_out}\d+)\s""",
        """mwg: \[({time}\d+/\w+/\d\d\d\d:\d\d:\d\d:\d\d [\+\-]\d+)\];\s*(|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?));\s*(|({http_response_code}\d+));\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?);\s*(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?);\s*(|\(({web_domain}[^;]+?)\));\s*(|\(-\)|\(({referrer}[^;]+?)\));\s*(|\(({categories}({category}[^,;]+)[^;]*?)\));\s*(|({=category}[^;]+?));\s*(|({mime}[^;]+?));\s*(|({bytes_in}\d+));\s*(|({bytes_out}\d+));\s*(|-|({rule}[^;]+?));\s*(|({failure_reason}[^;]+?));([^;]*;){2}\s*(|\(({method}\w+)\s+({url}(\w+:/+)?[^;\/]*?((?!(?:\d+\.){3}\d+)[^\.\s;]+(?:\.)+)?(:({=dest_port}\d+))?({uri_path}/[^;\?]*?)?({uri_query}\?[^;]*?)?)\s+\S+\));\s*(|({protocol}[^;]+?));\s*(|({user_agent}[^;]+?))(;|\s*$)""",
        """mwg: \[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [\+\-]\d+)\]"""
    ]
  

}
```