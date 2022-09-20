#### Parser Content
```Java
{
Name = mcafee-es-cef-file-write-success-removablestorage
      Vendor = McAfee
      Product = McAfee Endpoint Security
      TimeFormat = "epoch"
      Conditions = [ """McAfee|Data Loss Prevention""", """|DLP: Removable Storage Protection|""" ]
      Fields = [
        """(\s|\|)rt=({time}.+?)\s+([\w\.-]+=|$)""",
        """\d\d:\d\d\s+({host}[^\s]+)\sCEF:""",
        """(\s|\|)cs2=({device_type}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)dhost=({dest_host}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)dst=({dest_ip}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)duser=({user}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)dntdom=({domain}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)fname=.+?({file_name}[^\\]+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)filePath=({file_path}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)fsize=({bytes}\d+)\s+([\w\.-]+=|$)""",
        """(\s|\|)msg=({activity_details}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)msg=({operation}.+?)\s*([\w\.-]+=|$)""",
        """(\s|\|)msg=.+?to\s+({operation}[^,=]+)(,\s|\s|$)""",
        """(\s|\|)ad\.AppProductName =({process_name}.+?)\s+([\w\.-]+=|$)""",
      ]
	  ParserVersion = "v1.0.0"
    

}
```