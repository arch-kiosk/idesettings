# USTP - Upper Sabina Tiberina Project

Files and information for the customization of Kiosk and the FileMaker recording system for the Upper Sabina Tiberina Project.  
👉 please file issues and feature requests in [the office](https://github.com/arch-kiosk/arch-kiosk-office)

## release information

Since version 0.8.8 USTP has its own dataset definition in ustp_dsd3.yaml because the table collected_material_photos deviates from our standard definition:

```yaml
collected_material_photo:
structure:
  1:
    uid_cm: [datatype(UUID), join("collected_material")]
    uid_photo:
      [datatype(UUID), uid_file(), file_assigned_to("collected_material")]
    description: [datatype(VARCHAR), describes_file(uid_photo)]
    uid: [datatype(UUID), replfield_uuid()]
    created: [datatype(TIMESTAMP), replfield_created()]
    modified: [datatype(TIMESTAMP), replfield_modified()]
    modified_by: [datatype(VARCHAR), replfield_modified_by(), default('Null')]
```
The important difference here is the "file_assigned_to" directive.   

After every release you have to copy the ustp specific version to the standard dsd until we have a smarter mechanism.
