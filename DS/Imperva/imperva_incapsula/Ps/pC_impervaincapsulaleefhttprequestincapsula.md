#### Parser Content
```Java
{
Name = imperva-incapsula-leef-http-request-incapsula
  Vendor = Imperva
  Product = Imperva Incapsula
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """LEEF:""", """|Incapsula|SIEMintegration|""", """sourceServiceName =""", """cat=REQ_""" ]
  Fields = [
    """\Wstart=({time}\d{13})""",
    """\WsourceServiceName =({web_domain}.+?)\s+(\w+=|$)""",
    """\WsourceServiceName =[^\s\=]*?({top_domain}(?!(?:\d+\.){3}\d+)[^\.\s\/:]+(?=(?:\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za))+(\s|\/|$))[^\s\/]+)\s+(\w+=|$)""",
    """\Wsiteid=({site_id}.+?)\s+(\w+=|$)""",
    """\WrequestClientApplication=({user_agent}.+?)\s+(\w+=|$)""",
    """\WrequestClientApplication=[^=]*?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident)""",
    """\WrequestClientApplication=[^=]*?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wcs6=({app}.+?)\s+(\w+=|$)""",
    """\WcalCountryOrRegion=({country}.+?)\s+(\w+=|$)""",
    """\Wcicode=({city}.+?)\s+(\w+=|$)""",
    """\Wcs7=({latitude}.+?)\s+(\w+=|$)""",
    """\Wcs8=({longitude}.+?)\s+(\w+=|$)""",
    """\WCustomer=({user}.+?)\s+(\w+=|$)""",
# protocol_version is removed
    """\Wurl=(-|({url}(({protocol}[^:\\\/\s]+):[\\\/]+)?({web_domain}[^\\\/\s:]+)(:\d+)?({uri_path}\/[^\?"]*?)?({uri_query}\?[^"\s]*?)?))\s+(\w+=|$)""",
    """\WrequestMethod=({method}.+?)\s+(\w+=|$)""",
    """\Wproto=({protocol}.+?)\s+(\w+=|$)""",
    """\Wcat=({action}.+?)\s+(\w+=|$)""",
    """\WdeviceExternalId=({external_id}.+?)\s+(\w+=|$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
# xff_ip is removed
    """\Wcn1=({http_response_code}\d+)""",
    """\WdstPort=({dest_port}\d+)""",
    """\Win=({bytes_out}\d+)""",
    """\WsrcPort=({src_port}\d+)""",
  ]


}
```