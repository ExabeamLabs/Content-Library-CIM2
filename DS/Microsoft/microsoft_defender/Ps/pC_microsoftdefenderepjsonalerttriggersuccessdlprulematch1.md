#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-dlprulematch-1
  Vendor = Microsoft
  Product = Microsoft Defender
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"From":""", """"Workload":""", """"Actions":""", """"DlpRuleMatch"""" ]
  Fields = [
    """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"PolicyName":\s*"(|({alert_type}[^"]+))"(,|\})""",
    """"SensitiveInformation":\s*\[\{[^\}]*?"Location":\s*"(|({additional_info}[^"]+))"(,|\})""",
    """"Severity":\s*"({alert_severity}[^"]+)"""",
    """"IncidentId":\s*"({alert_id}[^"]+)"""",
    """"Actions":\s*\["({result}[^"]+)"""",
    """"RuleName":\s*"(|({alert_name}[^",\(]+?)\s*)("|\()""",
    """"FileName":\s*"(|({file_name}[^"]+))"(,|\})""",
    """"From":\s*"\s*\|?\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@"]+))?)""",
    """"To":\s*\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?")\]""",
    """"To":\s*\[({target}[^\]]+)\]""",
    """src-account-name":"({account_name}[^"]+)""",
    """Operation":\s*"({additional_info}[^"]+)"""",
    """"Workload":\s*"({alert_source}[^",]+)"""",
    """\ssuser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """FileSize":({bytes}\d+),""",
    """Subject":"({alert_subject}[^"]+?)\s*"""",
    """"SensitiveInformationTypeName":"({item_type}[^"]+)"""",
    """"SensitiveInformation":\\?\[\{.*?"Location"\s*:\s*((?!"Message Body")({email_attachments}"({email_attachment}[^',]+)[^"]*")),"\w+""""
    """exa_json_path=$.CreationTime,exa_field_name=time"""
    """exa_regex="CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.PolicyDetails.[0].PolicyName,exa_field_name=alert_type"""
    """exa_json_path=$.PolicyDetails.[0].Severity,exa_field_name=alert_severity"""
    """exa_regex="SensitiveInformation":\s*\[\{[^\}]*?"Location":\s*"(|({additional_info}[^"]+))"(,|\})"""
    """exa_json_path=$.IncidentId,exa_field_name=alert_id"""
    """exa_json_path=$.PolicyDetails.[0].Rules.[0].Actions,exa_field_name=result"""
    """exa_json_path=$.PolicyDetails.[0].RuleName,exa_field_name=alert_name"""
    """exa_json_path=$.ExchangeMetaData.From,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@"]+))?)"""
    """exa_regex="To":\s*\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?")\]"""
    """exa_regex="To":\s*\[({target}[^\]]+)\]""",
    """exa_json_path=$.Operation,exa_field_name=additional_info"""
    """exa_json_path=$.Workload,exa_field_name=alert_source"""
    """exa_json_path=$.ExchangeMetaData.FileSize,exa_field_name=bytes"""
    """exa_json_path=$.ExchangeMetaData.Subject,exa_field_name=alert_subject"""
    """exa_json_path=$.SharePointMetaData.FileName,exa_field_name=file_name"""
    """exa_json_path=$.SharePointMetaData.From,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@"]+))?)"""
    """exa_json_path=$.PolicyDetails.[0].Rules.[0].RuleName,exa_field_name=alert_name"""
    """exa_json_path=$.PolicyDetails.[0].Rules.[0].Severity,exa_field_name=alert_severity"""
    """exa_regex="SensitiveInformation":\\?\[\{.*?"Location"\s*:\s*((?!"Message Body")({email_attachments}"({email_attachment}[^',]+)[^"]*")),"\w+""""
    """exa_json_path=$..SensitiveInformationTypeName,exa_field_name=item_type"""
  ]
  ParserVersion = "v1.0.0"


}
```