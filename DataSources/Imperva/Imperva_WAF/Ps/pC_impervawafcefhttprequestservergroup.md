#### Parser Content
```Java
{
Name = imperva-waf-cef-http-request-servergroup
  Vendor = Imperva
  Product = Imperva WAF
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
    """src=(({src_ip}[A-Fa-f:\d]+)|({=src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\s""",
    """spt=({src_port}\d+)""",
    """dst=({dest_ip}[A-Fa-f:\d.]+)""",
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