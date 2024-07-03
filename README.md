# PBXware API Collection

Welcome to the PBXware API Collection repository! This collection includes a comprehensive set of API requests for interacting with the PBXware system. Whether you're a developer integrating PBXware functionality into your application or a system administrator looking to automate tasks, this collection provides you with the tools you need.

## Table of Contents

- [Overview](#overview)
- [How to Use](#how-to-use)
- [Folders Structure](#folders-structure)
- [License](#license)

### Overview

This repository provides a set of API requests and tests for the PBXware system. The requests are grouped into folders based on the various components of the PBXware system, with each folder containing requests related to a specific part of the system. Each request includes test cases to verify the functionality of the API endpoints.

### How to Use

To get started with the PBXware API Collection, follow these steps:

1. Clone the Repository

    bash: 
    git clone https://github.com/bicomsystems/PBXware-API-Documentation
    
    cd PBXware-API-Documentation

2. Open the Postman Collection

3. Import the Postman collection file (PBXware_API_Collection.postman_collection.json) into Postman to view and interact with the API requests. Instead of replacing the collection variables with the exact values, change the values of the collection variables themselves from the variables window.

4. Review the Documentation

    The full API documentation is available in the POSTMAN collection overview section and on your system under Admin Settings -> API Documentation. This section in POSTMAN provides detailed information on API endpoints, methods, parameters, and more.

5. Run Tests

6. Use Postman to run the tests with each request to verify the API’s functionality.

### Folders Structure

The requests are organized into the following folders with supported methods:

- Dashboard:
    - start - Start call recording for a specific extension
    - stop - Stop call recording for a specific extension
    - pause - Pause call recording for a specific extension
    - unpause - Unpause call recording for a specific extension
- Extensions:
    - list - List Extensions
    - configuration - Configuration of a specific extension
    - add - Add Extension
    - edit - Edit Extension
    - delete - Delete Extension
    - balance - Credit/Debit Balance
    - billing - Extension Billing (deprecated and will be soon replaced with call_rating)
    - billing_info - Extension Billing Info (deprecated and will be soon replaced with call_rating_info)
    - call_rating - Extension Call Rating
    - call_rating_info - Extension Call Rating Info
    - slaves - Returns all slaves extension for supplied master extension
    - billing_history - Billing History (deprecated and will be soon replaced with call_rating_history)
    - call_rating_history - Call Rating History
    - es - Extension Enhanced Services
    - reset_inclusive_minutes - Reset Inclusive Minutes
    - voicemail.delete - Delete Extension Voicemails
- Trunks:
    - list - List Trunks
    - configuration - Trunk Configuration
    - add - Add new Trunk
    - edit - Edit existing Trunk
    - providers - List Trunk Providers
- SMS:
    - reports- SMS and Bulk SMS reports
    - trunks - SMS Trunks management
    - trunks.tenants - SMS Trunks & Tenants management
- SMS and Bulk SMS reports:
    - list - List SMS
    - bulk_list - List Bulk SMS
- SMS Trunks:
    - list - List SMS Trunks
    - configuration - Configuration of specific SMS Trunk
    - add - Add SMS Trunk
    - edit - Edit SMS Trunk
    - delete - Delete SMS Trunk
- SMS Trunks & Tenants:
    - list - List SMS Trunks & Tenants
    - get - Get Tenant’s SMS Trunk
    - set - Set Tenant’s SMS Trunk
- DIDs:
    - list - List DIDs
    - add - Add new DID
    - edit - Edit existing DID
    - delete - Delete existing DID
    - clirouting.add - Add CLI Routing
    - clirouting.edit - Edit CLI Routing
    - clirouting.list - List CLI Routing
    - clirouting.delete - Delete CLI Routing
- DID Groups:
    - list - List DID Groups
    - add - Add new DID Group
    - edit - Edit existing DID Group
    - delete - Delete existing DID Group
- IVRs:
    - list - List IVRs
    - add - Add new IVR
    - edit - Edit existing IVR
    - delete - Delete existing IVR
- Ring Groups:
    - list - List Ring Groups
    - add - Add new Ring Group
    - edit - Edit existing Ring Group
    - delete - Delete existing Ring Group
    - configuration - Existing Ring Groupe configuration
- Enhanced Ring Groups:
    - add - Add/Create a new ERG
    - edit - Edit existing ERG
    - list - List Enhanced Ring Groups
    - members - Adding members to an Enhanced Ring Group
    - delete - Delete ERG
- CDRs:
    - download - Download CDRs
    - billamount - Returns the sum of billing amounts
- Archiving:
    - list - Listing Archives
- Routes:
    - list - List Routes
- Operation Times (DID, IVR, Dial Group, Server, Routes, Qoueues, ERG):
    - list - Listing the state of Operation Times
    - set - Set the state of Operation Times
- Tenant Packages:
    - configuration - Tenant Package Configuration
    - list - List Tenant Packages
    - add - Add new Tenant Package
    - edit - Edit existing Tenant Package
    - delete - Delete existing Tenant Package
- Tenants:
    - configuration - Tenant Configuration
    - list - List Tenants
    - add - Add new Tenant
    - edit - Edit existing Tenant
    - delete - Delete existing Tenant
    - trunks.list - List Trunks & Tenants
    - trunks.set - Set Trunks & Tenants
    - clirouting.add - Add CLI routing
    - clirouting.edit - Edit CLI routing
    - clirouting.list - List CLI routing
    - clirouting.delete - Delete CLI routing
- Servers:
    - configuration - Server Configuration
- Service plans:
    - list - List Service Plans
    - rates - List Service Plan Rates
- Destinations:
    - list - List Destinations
    - groups - List Destinations Groups
- UADs:
    - list - List UADs
    - activate - Activate UAD
    - deactivate - Deactivate UAD
- Apps:
    - list - List Apps
- Licence:
    - refresh - Refresh license
    - last_refreshed - Last time license file was modified
    - info - License information
- Monitor:
        list- List Monitor extensions
    - live_calls - List Live calls
- Departments:
    - list- List Destinations
- Call recording:
    - start - Start call recording for a specific extension
    - stop - Stop call recording for a specific extension
    - pause - Pause call recording for a specific extension
    - unpause - Unpause call recording for a specific extension

Each folder includes an overview window in Postman that details the methods supported for the specific feature and describes each request. Some folders may also contain additional subfolders for more straightforward navigation. For example, the SMS folder is divided into multiple subfolders, where we have the Adding SMS Trunks subfolder, which represents an Add method. This folder also contains subfolders for each SP. The same goes for the Editing SMS trunks.

### Additional note:
This GitHub repository includes CSV files that facilitate the bulk creation of objects (such as Extensions, DIDs, or ERGs). Each CSV file contains headers corresponding to the API collections' variables.

Key Rule: Ensure that the headers in your CSV file match the variables in the API requests.

Example: To create 100 Extensions, you can prepare a CSV file with headers that include all the required fields from the requests. Instead of static values, use the variable names as headers. Static values that remain constant across all entries can be specified directly in the API request.

By following this approach, you can efficiently manage and automate the creation of multiple objects using the provided CSV files.

If you use POSTMAN, go to any desired folder, right-click, and select Run folder. From the list, select the request you want to run. On the right side of the window, under the Functional tab, you have an option called Data, where you can upload your CSV file. Then, it's only left to Run the request.

Feel free to adjust the variables and CSV files according to your needs and wishes; these are the only templates used for testing purposes.

### License

This project is licensed under the MIT License.
