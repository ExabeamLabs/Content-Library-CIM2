#### Parser Content
```Java
{
Name = symantec-dlp-str-app-notification-vontusystemevent
   Vendor = Symantec
   Product = Symantec DLP
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ """Vontu System Event""", """ ["""]
   Fields= [
     """\w+\s+\d+ \d+:\d+:\d+\s+({event_name}.+?\])\s+({additional_info}.+?)\s*$""",
   ]
   ParserVersion = "v1.0.0"


}
```