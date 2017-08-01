# salesforce-rncontrol
Managed Router section in Sales Force

## Add Custom User fields
1. Navigate to "Setup" page. (Top right)
2. Click "Build->Customize->Users->Fields" (Left Menu)
3. Click "New" and create the following fields.

##### Domain Field
1. Data Type: Text
2. Field Label: rncontrol_domain
3. Length: 100
4. Field Name: rncontrol_domain
5. Keep default values for other settings and save.

##### Role Field
1. Data Type: Picklist
2. Field Label: rncontrol_role
3. Values: "admin", "domain-admin", "customer" (Separated by new line)
4. Field Name: rncontrol_role
5. Keep default values for other settings and save.

## Add RN-Control API URL to Salesforce
1. Navigate to "Setup" page. (Top right)
2. Click "Administer->Security Controls->Remote Site Settings" (Left Menu)
3. Click "New Remote Site" and fill in the following details.
    1. Remote Site Name: rn_control
    2. Remote Site URL: https://api.rncontrol.com
    3. Active: Keep it checked
4. Click "Save".

## Add Apex Class
All Apex classes used in this project are saved in the "Apex_classes" folder. They need to be added to Salesforce by following the steps below.

1. Navigate to "Developer Console".
2. Click "File->New->Apex Class".
3. Enter class name as filename and click "Ok".
4. Enter the Apex class code in the editor and save.
