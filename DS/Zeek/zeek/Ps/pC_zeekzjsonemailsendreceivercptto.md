#### Parser Content
```Java
{
Name = zeek-z-json-email-send-receive-rcptto
  ExtractionType = json
  ParserVersion = v1.0.0
  Conditions = [ 
"""id.orig_h"""
"""id.resp_h"""
"""mailfrom"""
"""rcptto"""
]
  Fields = ${ZeekParsersTemplates.json-bro-activity.Fields}[
    """"helo":\s*"({helo}[^"]+)""",
    """"mailfrom":\s*\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""""
    """rcptto":\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))".*?)\]""",
    """"subject":\s*"({email_subject}[^"]+)""",
    """"user_agent":\s*"({user_agent}[^"]+)""",
    """exa_json_path=$.helo,exa_field_name=helo""",
    """exa_json_path=$.mailfrom,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """exa_json_path=$.rcptto[:1],exa_regex=({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))".*?)""",
    """exa_regex=rcptto":\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))".*?)\]""",
    """exa_json_path=$.subject,exa_field_name=email_subject""",
    """exa_json_path=$.user_agent,exa_field_name=user_agent"""
  ]

json-bro-activity = {
  Vendor = Zeek
  Product = Zeek
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Fields = [
    """"ts\\?"+:[\[\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3,6}Z?)""",
    """"uid\\?"+:\\?"+({connection_id}[^"]+)""",
    """"id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"id\.orig_p\\?"+:({src_port}\d+)""",
    """"id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"id\.resp_p\\?"+:({dest_port}\d+)""",
    """"proto\\?"+:\\?"+({protocol}[^"]+)""",
    """exa_json_path=$.ts,exa_field_name=time""",
    """exa_json_path=$.uid,exa_field_name=connection_id""",
    """exa_regex="id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex="id\.orig_p\\?"+:({src_port}\d+)""",
    """exa_regex="id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_regex="id\.resp_p\\?"+:({dest_port}\d+)""",
    """exa_json_path=$.proto,exa_field_name=protocol"""
  
}
```