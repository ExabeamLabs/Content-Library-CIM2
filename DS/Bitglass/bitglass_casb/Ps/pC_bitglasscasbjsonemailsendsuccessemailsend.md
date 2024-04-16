#### Parser Content
```Java
{
Name = bitglass-casb-json-email-send-success-emailsend
  ParserVersion = v1.0.0
  Vendor = Bitglass
  Product = Bitglass CASB
  ExtractionType = json
  TimeFormat = "dd MMM yyyy HH:mm:ss"
  Conditions = [ """Email, Send, Web""", """ api.bitglass.com """, """"application":""", """"Office 365"""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.instancename,exa_field_name=host""",
    """exa_json_path=$.user,exa_regex=(({user}[\w\.\-]{1,40}\$?)|({full_name}[^",]+))""",
    """exa_json_path=$.email,exa_field_name=email_user""",
    """exa_json_path=$.device,exa_field_name=os""",
    """exa_json_path=$.application,exa_field_name=app""",
    """exa_json_path=$.ipaddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.filename,exa_regex=({file_name}[^"]+(\.({file_ext}[^."]+))?)""",
    """exa_json_path=$.useragent,exa_field_name=user_agent""",
    """exa_json_path=$.emailfrom,exa_regex=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.emailto,exa_field_name=email_recipients""",
    """exa_json_path=$.emailto,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.emailto,exa_regex=({external_address}[^",@]+@[^",]+)""",
    """exa_json_path=$.emailsubject,exa_field_name=email_subject"""
  ]


}
```