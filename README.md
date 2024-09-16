# SOAP-API-Test

[Countries SOAP API](http://webservices.oorsprong.org/websamples.countryinfo/CountryInfoService.wso?WSDL=) tested in SOAPUI Open Source Version. It involves groovy scripting for a data-driven test case which outputs a CSV file.

## Installation

Manually download the project, unzip it and then select `Import Project` from the `File` menu.

## Requirements
This project uses:

1. [opencsv](https://central.sonatype.com/artifact/com.opencsv/opencsv) to write the CSV Output file.
2. [list-of-countries.txt](https://gist.github.com/dariusz-wozniak/656f2f9070b4205c5009716f05c94067#file-list-of-countries-txt) from
[dariusz-wozniak](https://gist.github.com/dariusz-wozniak)'s GIST.
3. [Apache Ant](https://ant.apache.org/) to generate HTML Report.

The `list-of-countries.txt` is provided with the project, user's would have to download `opencsv` manually and place the jar file in `C:\Program Files\SmartBear\<SOAPUI-version-installation>\bin\ext`.

## Notes
The file `no-iso-countries.txt` was made by `Sunpreet Singh Rathor` during the build of this project.

## Usage - General
Since the project has a WSDL file, all requests are automatically added. This leads to running the project or it's components in a number of ways, such as:

1. Open a request, fill in the required fields and press `Submit` button. This sends a single request.
2. Double click `Initial Suite` and press the `Run` button to execute the test suite.
3. Double click a Test Case and press `Run` button to execute all Test Steps within the selected Test Case.
4. Open a request within a Test Case, fill in the required information and press `Submit`. Assertions can directly be added here.

## Usage - HTML Report
To generate the HTML Report, edit the `build.xml` to specify the following:

1. SOAPUI Installation Folder
2. Apache Ant Installation Folder
3. Current Project Folder

After these have been updated, run the command `ant` in the project folder in Command Prompt or PowerShell. The HTML Report would be generated in `HTML` folder of the project directory.

## License

[MIT](https://choosealicense.com/licenses/mit/)