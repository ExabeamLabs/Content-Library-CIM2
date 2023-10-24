#### Parser Content
```Java
{
Name = "microsoft-o365-csv-app-activity-success-onedrive"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
""","OneDrive","20"""
""","SharePoint",""""
]
Fields = [
""",\"({app}OneDrive)\",\"\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)?Z\"(,(\"[^\"]*\"|[^,]*)){2

}
```