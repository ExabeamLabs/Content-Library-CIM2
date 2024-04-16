#### Parser Content
```Java
{
Name = symantec-wss-json-http-session-queryresponse
  Vendor = Symantec
  Product = Symantec Web Security Service
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ ""","Query_Response":"""", ""","CommandID":"""", """"Response_Code":"""" ]
  Fields = [
    """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"host":"(|({host}[\w\-.]+))"""",
    """"DomainID":"({web_domain}[^"]+)""",
    """"User_Agent":"({user_agent}[^"]+)""",
    """"CommandID":"({method}[^"]+)""",
    """"UserIDSrc":"({user}[\w\.\-]{1,40}\$?)""",
    """"Response_Code":"({http_response_code}\d+)""",
    """"Category":"({category}[^"]+)""",
    """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"src_port":({dest_port}\d+)""",
    """"Query_Response":"({action}[^"]+)""",
    """"sig":.+?"name":"({proxy_action}[^"]+)""",
    """"URL":"({uri_path}[^"]+)""",
    """"Bytes_Sent":({bytes_out}\d+)""",
    """"Bytes_Received":({bytes_in}\d+)""",
    """"AppID":"({mime}[^"]+)""",
    """"Destination_Logon_ID":"({app_user}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```