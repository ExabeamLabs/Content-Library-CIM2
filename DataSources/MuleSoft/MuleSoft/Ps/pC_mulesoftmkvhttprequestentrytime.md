#### Parser Content
```Java
{
Name = mulesoft-m-kv-http-request-entrytime
  ParserVersion = "v1.0.0"
  Vendor = MuleSoft
  Product = MuleSoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = ["""snb-mule-api""", """"Source System":""", """Entry Time"""]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}).*?\s+({host}[^\s]+)\s""",
    """"Entry Time":\s*("|\|)(NA|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}))""",
    """"Method":\s*"({method}[^"]+)""",
    """"host":\s*"({web_domain}[^"]+)""",
    """"Target System":\s*"(NA|({dest_host}[^"]+))""",
    """"Source System":\s*"(NA|({src_host}[^"]+))""",
    """"Request path":\s*"({uri_path}[^"]+)""",
    """"Service Name":\s*"({category}[^"]+)""",
    """"Response Status Code":\s*({result_code}\d+)""",
    """"Error Message":\s*"(NA|({failure_reason}[^",]+))""",
    """"Query"+:\s*\{\s*(|({uri_query}[^\}]+?))\s*\}""",
    """mimeType:\s*"*({mime}[^:]+?)"*,\s+\w+:""",
    """(CardAcctRelInfo[^\}\]]*)?AcctId"+:\s*"+({account_id}[^"]+)""",
    """(CardAcctRelInfo[^\}\]]*)?AcctType"+:\s*"+({user_type}[^"]+)""",
    """firstName"+:\s*"+({first_name}[^"]+)""",
    """lastName"+:\s*"+({last_name}[^"]+)""",
# check_serial_num is removed
# check_amount is removed
# card_id is removed
# tax_id is removed
# document_id is removed
# confirmation_code is removed
# transfer_id is removed
# party_id is removed
    """correlationId="+({correlation_id}[^"]+)""",
    """"user-agent":\s*"({user_agent}[^"]+)""",
    """"user-agent":.+?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)"""
  ]


}
```