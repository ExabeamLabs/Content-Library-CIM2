#### Parser Content
```Java
{
Name = microsoft-azuremon-kv-app-activity-uam
   ParserVersion = "v1.0.0"
   Vendor = Microsoft
   Product = Azure Monitor
   TimeFormat = "MM/dd/yyyy HH:mm:ss"
   Conditions = [  """ ORIGIN=""", """ TYPE=""", """ USER=""", """ UAM """ ]
   Fields = [
      """\sEVENT=({action}.+?)\s*\w+="""
      """\sTYPE=({category}.+?)\s*\w+=""",
      """\sUSER=([\s\w]*\\)?({user}[\w\.\-]{1,40}\$?)\s*\w+=""",
# origin is removed
      """\sDETAILS=time=({time}\d{1,2}\/\d{1,2}\/\d{1,4}\s\d{1,2}:\d{1,2}:\d{1,2})""",
   ]


}
```