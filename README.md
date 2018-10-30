# Copy To Clipboard

This project contains sample code to demonstrate how to copy text to the clipboard in an Aras client-side action. It also demonstrates how to use PE_GetSelectedItems to execute an action on multiple selected items in the Aras Innovator client.

Note: The sample method was developed using the Part ItemType, but it can be easily adapted for any ItemType.

## History

Release | Notes
--------|--------
[v1.1.0](https://github.com/ArasLabs/copy-to-clipboard/releases/tag/v1.1.0) | Confirmed support for Aras 11 SP15.
[v1.0](https://github.com/ArasLabs/copy-to-clipboard/releases/tag/v1.0) | First release. Includes sample code to use the action with the Part, CAD, and/or Document ItemTypes.

#### Supported Aras Versions

Project | Aras
--------|------
[v1.1.0](https://github.com/ArasLabs/copy-to-clipboard/releases/tag/v1.1.0) | 11.0 SP15, 11.0 SP14, 11.0 SP12
[v1.0](https://github.com/ArasLabs/copy-to-clipboard/releases/tag/v1.0) | 11.0 SP12

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed (version 11.0 SPx preferred)
2. Aras Package Import tool
3. CopyToClipboard import package

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
    * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
    * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\CopyToClipboard\Import\imports.mf` file in the Manifest File field.
6. Select **CopyToClipboard** in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.
10. Login to Aras as an administrator (i.e. admin).
11. Navigate to **Administration > ItemTypes** in the TOC.
12. Open the ItemType you want to add the action to. The sample code was developed for the Part ItemType, but will work OOTB for CAD and Document as well.
13. In the ItemType, add the Copy to Clipboard action to the Actions tab.
14. Save your changes to the ItemType.

You are now ready to login to try out the Copy To Clipboard action.

## Usage

![Demo](Screenshots/demo.gif)

1. Log in to Aras.
2. Navigate to the ItemType you added the action to in the setup steps.
3. Select one or more items in the main grid. (Use Ctrl+click to pick more than one.)
4. Right click on a selected item and choose **Copy to Clipboard**. 

If you are using a browser that allows programmatic access to the clipboard (IE, Chrome), the selected item(s) info will be copied to the clipboard. If you are using a browser that does not allow clipboard access, you will see a dialog appear with the item info and an instruction to copy the content using Ctrl+C.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.

## Credits

Created by Eli Donahue for Aras Labs. @EliJDonahue

## License

Aras Labs projects are published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
