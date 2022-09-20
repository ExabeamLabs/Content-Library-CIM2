#### Parser Content
```Java
{
Name = mcafee-wg-json-http-session-amwprobability
    ParserVersion = v1.0.0
    Vendor = McAfee
    Product = McAfee Web Gateway
    TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
    Conditions = [ """"pxyOutAd":"""", """pxyPort":"""",""""urlLongCat":""",""""amwProbability":"""  ]
    Fields = [
        """"timeStamp":"\[({time}\d+\/\w+\/\d{4}:\d\d:\d\d:\d\d (\+|\-)\d{4})\]"""",
        """"dstURL":"({url}\w+:\/\/[^:\/"]+(:({dest_port}\d+))?({uri_path}\/[^\?"]*)?({uri_query}\?[^"]*)?)"""",
        """"urlLongCat":"({categories}({category}[^",]+)[^"]*)"""",
        """"connSrc":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
        """"connDst":"({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
        """"urlHost":"(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^"]+))"""",
        """"authUser":"(?:\([^\)]+\)|({user}[^"]+))"""",
        """"blkReason":"({failure_reason}[^"]+)"""",
        """"authMethod":"({auth_method}[^"]+)"""",
        """"authStatus":"({authenticated}[^"]+)"""",
        """FailMsg":"({failure_msg}[^"]+)"""",
        """"cheStatus":"({proxy_action}[^"]+)"""",
        """"headUsrAgt":"({user_agent}[^"]+)"""",
        """"mediaPbly":"({mime}[^"]+)"""",
        """"respStatus":"({http_response_code}\d+)"""",
        """"connRunTime":"({conn_duration}[^"]+)"""",
        """"urlCat":"({category_id}[^"]+)"""",
        """"connProto":"({protocol}[^"]+)"""",
        """"pxyPort":"({src_port}\d+)"""",
        """"byteP2C":"({bytes_out}\d+)"""",
        """"byteC2P":"({bytes_in}\d+)"""",
    ]


}
```