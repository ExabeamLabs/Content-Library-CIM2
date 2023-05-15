#### Parser Content
```Java
{
Name = imperva-securesphere-cef-http-request-servergroup
  Vendor = Imperva
  Product = Imperva SecureSphere
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """RequestParameters""", """cs4Label=MxIP""", """|Imperva Inc.|SecureSphere""", """cat=Alert""", """cs1Label=ServerGroup""" ]
  Fields = [
    """rt=({time}\w{3}\s\d+\s\d+\s\d+:\d+:\d+)""",
    """cs1=({server_group}[^\s]+)""",
    """cs2=({service_name}[^\s]+)""",
# mx_ip is removed
    """duser=({user}[^\s]+)""",
    """deviceExternalId=({external_id}[^\s]+)""",
    """cs3=({app}[^\s]+)""",
    """requestClientApplication=({app}[^=]+?)\s(\w+=|$)""",
    """country_code[\\\=]*({country}[^,]+)""",
    """src=(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)|({=src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s""",
    """spt=({src_port}\d+)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """dpt=({dest_port}\d+)""",
    """reason=({event_category}[^\s]+)""",
    """requestMethod=({method}[^=]+?)\s+(\w+=|$)""",
    """response-code"[\\=]*"({http_response_code}\d+)""",
    """response-size"[\\=]*"({bytes_out}\d+)""",
    """request=(-|({url}(({protocol}[^:\\\/\s]+):[\\\/]+)?(\?|({web_domain}[^\\\/\s:]+))(:\d+)?({uri_path}\/[^\?"]*?)?({uri_query}[^"\s]*?)?))(\s+\w+=|\s*$)""",
    """proto=({protocol}[^\s]+)""",
    """\Wcat=({action}[^=]+?)\s(\w+=|$)""",
    """CEF:([^\|]+\|){4}Custom\|({operation}[^\|]+)\|""",
    """CEF:([^\|]+\|){4}Custom\|[^\|]+\|({risk_level}\d+)""",
   ]


}
```