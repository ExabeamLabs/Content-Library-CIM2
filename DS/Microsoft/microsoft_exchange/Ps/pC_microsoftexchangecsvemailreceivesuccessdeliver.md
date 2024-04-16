#### Parser Content
```Java
{
Name = microsoft-exchange-csv-email-receive-success-deliver
Vendor = Microsoft
Product = Microsoft Exchange
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """,STOREDRIVER,DELIVER,"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)Z,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){6}STOREDRIVER,DELIVER,"""
  """,({host}[^\s,]+),(?:(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|,){3}STOREDRIVER,DELIVER,"""
  """,[^\s,]+:({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){3}STOREDRIVER,DELIVER,"""
  """,\s*(?:'|")?({host}[\w\.-]+)(?:'|")?\s*,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){2}STOREDRIVER,DELIVER,"""
  """({alert_name}STOREDRIVER,DELIVER)"""
  """,STOREDRIVER,DELIVER,\s*({alert_id}\d+)\s*,"""
  """,STOREDRIVER,DELIVER,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){2}\s*(?:'|")?({email_recipients}[^,]+?)\s*(?:'|")?,"""
  """,STOREDRIVER,DELIVER,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){2}\s*(?:'|")?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({orig_user}[\w\.\-]{1,40}\$?))[^,]*?\s*(?:'|")?,"""
  """,STOREDRIVER,DELIVER,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){4}\s*({bytes}\d+)\s*,"""
  """,STOREDRIVER,DELIVER,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){5}\s*({num_recipients}\d+)\s*,"""
  """,STOREDRIVER,DELIVER,(?:(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){8}\s*({email_subject}[^,]+)\s*,"""
  """,STOREDRIVER,DELIVER,(?:(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){8}\s*'({email_subject}(?:[^']|'')+)'\s*,"""
  """,STOREDRIVER,DELIVER,(?:(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){8}\s*"({email_subject}(?:[^"]|"")+)"\s*,"""
  """,STOREDRIVER,DELIVER,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){9}\s*(?:'|")?(|MicrosoftExchange.*?|({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:'|")?)\s*,"""
  """,STOREDRIVER,DELIVER,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){10}\s*(?:'|")?(?:<>|({return_path}[^,]+?))(?:'|")?\s*,"""
]
DupFields = [
  "orig_user->user"
  "alert_name->alert_type"
  "src_email_address->external_address"
]
ParserVersion = "v1.0.0"


}
```