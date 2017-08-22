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

## Create Managed Router Custom Object
1. Navigate to "Setup" page. (Top right)
2. Click "Build->Create->Objects" (Left Menu)
3. Click the "New Custom Object" button and fill in the following details.
    1. Label: Managed Router
    2. Plural Label: Managed Routers
    3. Object Name: Managed_Router
    4. Record Name: Name
    5. Data Type: Text
4. Click "Save" button.

#### Add Fields to Managed Router Custom Object
1. Navigate to "Setup" page. (Top right)
2. Click "Build->Create->Objects" (Left Menu)
3. Click "Managed Router" from the list.
4. Under the "Custom Fields & Relationships" section, click the "New" button. (Repeat these steps to create the following fields).
    1. **RNControlID**
        1. Data Type: Number
        2. Length: 18
        3. Decimal Places: 0
        4. Field Name: RNControlID
        5. Required, Unique, External ID: Checked
        6. Keep default values for all other fields and save.
    2. **Domain**
        1. Data Type: Text
        2. Field Label: Domain
        3. Length: 255
        4. Field Name: Domain
        5. Required: Checked
        6. Keep default values for all other fields and save.
    3. **Serial**
        1. Data Type: Text
        2. Field Label: Serial
        3. Length: 255
        4. Field Name: Serial
        5. Required: Checked
        6. Keep default values for all other fields and save.
    4. **Mac**
        1. Data Type: Text
        2. Field Label: Mac
        3. Length: 255
        4. Field Name: Mac
        5. Required: Checked
        6. Keep default values for all other fields and save.
    5. **Make**
        1. Data Type: Text
        2. Field Label: Make
        3. Length: 255
        4. Field Name: Make
        5. Required: Checked
        6. Keep default values for all other fields and save.
    6. **Model**
        1. Data Type: Text
        2. Field Label: Model
        3. Length: 255
        4. Field Name: Model
        5. Required: Checked
        6. Keep default values for all other fields and save.
    7. **Url**
        1. Data Type: URL
        2. Field Label: Url
        3. Field Name: Url
        4. Required: Checked
        5. Keep default values for all other fields and save.
    8. **Contact**
        1. Data Type: Lookup Relationship
        2. Related To: Contact
        3. Field Label: Contact
        4. Field Name: Contact
        5. Child Relationship Name: Managed_Routers
        6. Keep default values for all other fields and save.

## Add Apex Classes
All Apex classes used in this project are saved in the "Apex_classes" folder. They need to be added to Salesforce by following the steps below.

1. Navigate to "Developer Console".
2. Click "File->New->Apex Class".
3. Enter class name as filename and click "Ok".
4. Enter the Apex class code in the editor and save.
5. Repeat above steps for all files in "Apex_classes" folder.

## Add Visualforce Pages
All Visualforce pages used in this project are saved in the "Visualforce_pages" folder. They need to be added to Salesforce by following the steps below.

1. Navigate to "Developer Console".
2. Click "File->New->Visualforce Page".
3. Enter the filename and click "Ok".
4. Enter the code in the editor and save.
5. Repeat above steps for all files in "Visualforce_pages" folder.

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

## Create Add Managed Router Custom tab
This tab will display the "AddRNControlRouter" Visualforce page. To create the tab, follow the steps below.

1. Navigate to "Setup" page. (Top right)
2. Click "Build->Create->Tabs" (Left Menu)
3. In the "Visualforce Tabs" section, click the "New" button.
4. Use the following settings.
    1. Visualforce Page: AddRNControlRouter
    2. Tab Label: Add Managed Router
    3. Tab Name: Add_Managed_Router
    4. Tab Style: Choose any
    5. Select the profiles who should have access to this page.
    6. In the "Add to Custom Apps" section, check the new RN Control (RN_Control) app.
5. After saving, the new Add Managed Router tab will appear in the RN Control application page.
