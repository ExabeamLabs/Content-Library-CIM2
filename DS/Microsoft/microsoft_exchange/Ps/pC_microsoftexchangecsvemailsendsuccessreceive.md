#### Parser Content
```Java
{
Name = "microsoft-exchange-csv-email-send-success-receive"
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
""",STOREDRIVER,RECEIVE,"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)Z,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){6}STOREDRIVER,RECEIVE,"""
""",({host}[^\s,]+),(?:(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|,){3}STOREDRIVER,RECEIVE,"""
""",[^\s,]+:({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){3}STOREDRIVER,RECEIVE,"""
""",\s*(?:'|\")?({host}[\w\.-]+)(?:'|\")?\s*,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){2}STOREDRIVER,RECEIVE,"""
"""({additional_info}STOREDRIVER,RECEIVE)"""
""",STOREDRIVER,RECEIVE,\s*({alert_id}\d+)\s*,"""
""",STOREDRIVER,RECEIVE,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){2}\s*(?:'|\")?({email_recipients}({dest_email_address}[^;,]+)[^,]+?)\s*(?:'|\")?,"""
""",STOREDRIVER,RECEIVE,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){2}\s*(?:'|\")?({external_address}[^;@]+@[^;,\"']+)[^,]*?\s*(?:'|\")?,"""
""",STOREDRIVER,RECEIVE,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){4}\s*({bytes}\d+)\s*,"""
""",STOREDRIVER,RECEIVE,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){5}\s*({num_recipients}\d+)\s*,"""
""",STOREDRIVER,RECEIVE,(?:(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){8}\s*({email_subject}[^,]+)\s*,"""
""",STOREDRIVER,RECEIVE,(?:(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){8}\s*'({email_subject}(?:[^']|'')+)'\s*,"""
""",STOREDRIVER,RECEIVE,(?:(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){8}\s*\"({email_subject}(?:[^\"]|\"\")+)\"\s*,"""
""",STOREDRIVER,RECEIVE,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){9}\s*(?:'|\")?({email_address}[^,]+?)(?:'|\")?\s*,"""
""",STOREDRIVER,RECEIVE,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*\"(?:[^\"]|\"\")+\")\s*,|[^\",]+?,|\s*,){10}\s*(?:'|\")?(?:<>|({return_path}[^,]+?))(?:'|\")?\s*,"""
]
DupFields = [
"email_address->src_email_address"
]
ParserVersion = "v1.0.0"


}
```