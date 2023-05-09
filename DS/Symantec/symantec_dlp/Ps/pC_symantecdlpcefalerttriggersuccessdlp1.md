#### Parser Content
```Java
{
Name = symantec-dlp-cef-alert-trigger-success-dlp-1
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = "MMMM dd, yyyy HH:mm:ss"
    Conditions = [ """CEF""","""|Symantec|DLP|""","""Application_Name =""","""Sender=""" ]
    Fields = [
      """({host}[\w\-.]+)\s+CEF:""",
      """Occurred_On="({time}\w+\s\d{1,2

}
```