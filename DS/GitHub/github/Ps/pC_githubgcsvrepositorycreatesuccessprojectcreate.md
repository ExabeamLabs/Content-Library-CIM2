#### Parser Content
```Java
{
Name = github-g-csv-repository-create-success-projectcreate
   ParserVersion = v1.0.0
   Vendor = GitHub
   Product = GitHub
   TimeFormat = "epoch"
   Conditions = [ """project.create,""" ]
   Fields = [
     """({operation}project.create),({user}[\w\.\-\!\#\^\~]{1,40}\$?),(?:\s*|({resource}[^,]*)),[^,]*,(?:\s*|({object}[^,]*)),({time}\d{13}),[^,]*,(?:\s*|("*\[)?({additional_info_2}[^\[\]]*)(\]"*)?),([^,]*,){3}(?:\s*|({additional_info_1}.*?))\s*$""" 
  ]


}
```