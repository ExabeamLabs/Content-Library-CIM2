#### Parser Content
```Java
{
Name = mcafee-wg-csv-http-session-3
    ParserVersion = "v1.0.0"
    Vendor = McAfee
    Product = McAfee Web Gateway
    TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
    Conditions = [ """mwg: [""", """);""" ]
    Fields = [
        """mwg: \[({time}\d+/\w+/\d\d\d\d:\d\d:\d\d:\d\d [\+\-]\d+)\];\s*(|-|({user}[^;]+?));\s*(|({http_response_code}\d+));\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?);\s*(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?);\s*(|\(({web_domain}[^;]+?)\));\s*(|\(-\)|\(({referrer}[^;]+?)\));\s*(|\(({categories}({category}[^,;]+)[^;]*?)\));\s*(|({=category}[^;]+?));\s*(|({mime}[^;]+?));\s*(|({bytes_in}\d+));\s*(|({bytes_out}\d+));\s*(|-|({rule}[^;]+?));\s*(|({failure_reason}[^;]+?));([^;]*;){2}\s*(|\(({method}\w+)\s+({url}(\w+:/+)?[^;\/]*?((?!(?:\d+\.){3}\d+)[^\.\s;]+(?:\.)+)?(:({=dest_port}\d+))?({uri_path}/[^;\?]*?)?({uri_query}\?[^;]*?)?)\s+\S+\));\s*(|({protocol}[^;]+?));\s*(|({user_agent}[^;]+?))(;|\s*$)""",
    ]
  

}
```