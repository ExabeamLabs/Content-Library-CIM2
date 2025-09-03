#### Parser Content
```Java
{
Name = stealthbits-s-kv-app-activity-activedirectory
  ParserVersion = "v1.0.0"
  Conditions = [ """StealthINTERCEPT""", """Event_Source="Active Directory"""", """ObjectClass="""", """ SuccessfulChange="""" ]
  Fields = ${StealthBitsParsersTempletes.stealthintercept-ad-events.Fields} [
    """\sDistinguishedName =\"({user_ou}[^\"]+)\""""
  ]


}
```