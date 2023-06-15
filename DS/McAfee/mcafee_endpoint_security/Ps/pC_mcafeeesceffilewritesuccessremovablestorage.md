#### Parser Content
```Java
{
Name = mcafee-es-cef-file-write-success-removablestorage
      Vendor = McAfee
      Product = McAfee Endpoint Security
      TimeFormat = "epoch"
      Conditions = [ """McAfee|Data Loss Prevention""", """|DLP: Removable Storage Protection|""" ]
      Fields = [
        """(\s|\|)rt=({time}\d{13})\s+([\w\.-]+=|$)""",
        """\d\d:\d\d\s+({host}[^\s]+)\sCEF:""",
        """(\s|\|)cs2=({device_type}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)dhost=({dest_host}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+([\w\.-]+=|$)""",
        """(\s|\|)duser=({user}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)dntdom=({domain}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)fname=.+?({file_name}[^\\]+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)filePath=({file_path}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)fsize=({bytes}\d+)\s+([\w\.-]+=|$)""",
        """(\s|\|)msg=({operation_details}.+?)\s+([\w\.-]+=|$)""",
        """(\s|\|)msg=({operation}.+?)\s*([\w\.-]+=|$)""",
        """(\s|\|)msg=.+?to\s+({operation}[^,=]+)(,\s|\s|$)""",
        """(\s|\|)ad\.AppProductName =({process_name}.+?)\s+([\w\.-]+=|$)""",
      ]
	  ParserVersion = "v1.0.0"
    

}
```