#### Parser Content
```Java
{
Name = "github-g-csv-repository-modify-success-update"
Vendor = "GitHub"
Product = "GitHub"
TimeFormat = "epoch"
Conditions = [
"""issue_comment.update,"""
]
Fields = [
"""({operation}[^,]+),({user}[^,]+),(?:\s*|({resource}[^,]*)),[^,]*,(?:\s*|({object}[^,]*)),({time}\d{13}),[^,]*,(?:\s*|("*\[)?({additional_info_2}[^\[\]]*)(\]"*)?),([^,]*,){3}(?:\s*|({additional_info_1}.*?))\s*$"""
]
ParserVersion = "v1.0.0"


}
```