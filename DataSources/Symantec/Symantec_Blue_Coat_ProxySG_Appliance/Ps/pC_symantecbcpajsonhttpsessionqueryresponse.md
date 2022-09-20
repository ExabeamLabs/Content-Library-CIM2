#### Parser Content
```Java
{
Name = symantec-bcpa-json-http-session-queryresponse
  Vendor = Symantec
  Product = Symantec Blue Coat ProxySG Appliance
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ ""","Query_Response":"""", ""","CommandID":"""", """"Response_Code":"""" ]
  Fields = [
    """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"host":"(|({host}[\w\-.]+))"""",
    """"DomainID":"({web_domain}[^"]+)""",
    """"User_Agent":"({user_agent}[^"]+)""",
    """"CommandID":"({method}[^"]+)""",
    """"UserIDSrc":"({user}[^"]+)""",
    """"Response_Code":"({http_response_code}\d+)""",
    """"Category":"({category}[^"]+)""",
    """"src_ip":"({src_ip}[A-Fa-f:\d.]+)""",
    """"dst_ip":"({dest_ip}[A-Fa-f:\d.]+)""",
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