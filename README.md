# salesforce-rncontrol
Managed Router section in Sales Force

## Add Custom User fields
1. Navigate to "Setup" page. (Top right)
2. Click "Build->Customize->Users->Fields" (Left Menu)
3. Click "New" and create the following fields.

#### Domain Field
1. Data Type: Text
2. Field Label: rncontrol_domain
3. Length: 100
4. Field Name: rncontrol_domain
5. Keep default values for other settings and save.

#### Role Field
1. Data Type: Picklist
2. Field Label: rncontrol_role
3. Values: "admin", "domain-admin", "customer" (Separated by new line)
4. Field Name: rncontrol_role
5. Keep default values for other settings and save.
