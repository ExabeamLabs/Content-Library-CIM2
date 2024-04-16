#### Parser Content
```Java
{
Name = passwordmngrpro-p-str-app-activity-success-harmfulcontententered
  ParserVersion = v1.0.0
  Product = Password Manager Pro
  Vendor = Password Manager Pro
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [  """ Harmful_Content_Entered ""","""PMP_detected_harmful_content_in_the_data_entered_by_the_user_and_aborted_the_operation._Contents_of_the_user_input_""" ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s(ResourceAudit|UserAudit):[^:]+:(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-\.]+))\s({event_name}[\w\_]+)\s""",
    """({time}\d\d\d\d(\\)?\/\d\d(\\)?\/\d\d\s\d\d:\d\d:\d\d)\s({result}[\w]+)\s({src_host}[\w\-\.]+)"""
  ]


}
```