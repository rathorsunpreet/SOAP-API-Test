# SOAP-API-Test

[Countries SOAP API](http://webservices.oorsprong.org/websamples.countryinfo/CountryInfoService.wso?WSDL=) tested in SOAPUI Open Source Version. It involves groovy scripting for a data-driven test case which outputs a CSV file.

## Installation

Either manually download the project and then select `Import Project` or use `Import Remote Project` from the `File` menu.

## Requirements
This project uses [opencsv](https://central.sonatype.com/artifact/com.opencsv/opencsv) to write the CSV Output file and [list-of-countries.txt](https://gist.github.com/dariusz-wozniak/656f2f9070b4205c5009716f05c94067#file-list-of-countries-txt) from
[dariusz-wozniak](https://gist.github.com/dariusz-wozniak)'s GIST.

The `list-of-countries.txt` is provided with the project, user's would have to download `opencsv` manually and place the jar file in `C:\Program Files\SmartBear\<SOAPUI-version-installation>\bin\ext`.

## Notes
The file `no-iso-countries.txt` was made by `Sunpreet Singh Rathor` during the build of this project.

## Usage
Since the project has a WSDL file, all requests are automatically added. This leads to running the project or it's components in a number of ways, such as:

1. Open a request, fill in the required fields and press `Submit` button. This sends a single request.
2. Double click `Initial Suite` and press the `Run` button to execute the test suite.
3. Double click a Test Case and press `Run` button to execute all Test Steps within the selected Test Case.
4. Open a request within a Test Case, fill in the required information and press `Submit`. Assertions can directly be added here.

## License

[MIT](https://choosealicense.com/licenses/mit/)