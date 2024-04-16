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
""",\"({app}OneDrive)\",\"\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)?Z\"(,(\"[^\"]*\"|[^,]*)){2},\"[^\"]*?({email_address}[^\"\|]+)\"(,[^,]*){10},\"({operation}[^\"]+)\",((\"[^\"]*\"|[^,]*),){3}\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\",((\"[^\"]*\"|[^,]*),){7}(|\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\"),.*?,\"SharePoint\",((\"[^\"]*\"|[^,]*),){10}(|\"({share_path}[^\"]+)\"),(|\"({file_name}[^\"]+?(\.({file_ext}\w+))?)\"),(|\"({file_dir}[^\"]+)\"),"""
]
DupFields = [
"operation->access"
]
ParserVersion = "v1.0.0"


}
```