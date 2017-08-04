# salesforce-rncontrol
Managed Router section in Sales Force

## Add Custom User fields
1. Navigate to "Setup" page. (Top right)
2. Click "Build->Customize->Users->Fields" (Left Menu)
3. Click "New" button in "User Custom Fields" section and create the following fields.

##### RN Control Username Field
1. Data Type: Text
2. Field Label: rncontrol_username
3. Length: 255
4. Field Name: rncontrol_username
5. Keep default values for other settings and save.

##### RN Control Password Field
1. Data Type: Text (Encrypted)
2. Field Label: rncontrol_password
3. Length: 175
4. Field Name: rncontrol_password
5. Mask Type: Mask All Characters
6. Mask Character: *
7. Keep default values for other settings and save.

## Add RN-Control API URL to Salesforce
1. Navigate to "Setup" page. (Top right)
2. Click "Administer->Security Controls->Remote Site Settings" (Left Menu)
3. Click "New Remote Site" and fill in the following details.
    1. Remote Site Name: rn_control
    2. Remote Site URL: https://api.rncontrol.com
    3. Active: Keep it checked
4. Click "Save".

## Add Apex Classes
All Apex classes used in this project are saved in the "Apex_classes" folder. They need to be added to Salesforce by following the steps below.

1. Navigate to "Developer Console".
2. Click "File->New->Apex Class".
3. Enter class name as filename and click "Ok".
4. Enter the Apex class code in the editor and save.

## Add Visualforce Pages
All Visualforce pages used in this project are saved in the "Visualforce_pages" folder. They need to be added to Salesforce by following the steps below.

1. Navigate to "Developer Console".
2. Click "File->New->Visualforce Page".
3. Enter the filename and click "Ok".
4. Enter the code in the editor and save.

## Create RN Control Salesforce Application
To group all RN Control related tabs and features together, a new Salesforce application can be created. Follow the steps below to create a new Salesforce application.

1. Navigate to "Setup" page. (Top right)
2. Click "Build->Create->Apps" (Left Menu)
3. In the "Apps" section, click the "New" button.
4. Use the following settings.
    1. Type: Custom app
    2. App Label: RN Control
    3. App Name: RN_Control
    4. Make sure to set app visibility to required profiles.
5. After saving the app, you can switch to the newly created app from the App menu at the top right corner.

## Create Managed Routers Custom tab
This tab will display the "ListRNControlRouters" Visualforce page. To create the tab, follow the steps below.

1. Navigate to "Setup" page. (Top right)
2. Click "Build->Create->Tabs" (Left Menu)
3. In the "Visualforce Tabs" section, click the "New" button.
4. Use the following settings.
    1. Visualforce Page: ListRNControlRouters
    2. Tab Label: Managed Routers
    3. Tab Name: Managed_Routers
    4. Tab Style: Choose any
    5. Select the profiles who should have access to this page.
    6. In the "Add to Custom Apps" section, check the new RN Control (RN_Control) app.
5. After saving, the new Managed Routers tab will appear in the RN Control application page.
