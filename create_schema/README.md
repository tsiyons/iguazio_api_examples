# CreateSchema

Scans records in an existing table, and create the .#schema file from it.

Run ./create_schema --help for full usage

## Change-log
### Initial version
* All features are supported via command line arguments
* Supports http and https over default and custom ports
* Supports both authentication and authenticationles operation
* Supports partitioning by allowing to specify a different path for the output file
* Supports paralellism of NoSQL requests for optimal performance
* Supports dry-run - no actual write

### Known Limitations:
* Data type double is written as long in the .#schema file due to inability to distinguish between long and double using GetItems calls
* Program scans records read (based on limit provided) for consistency of attributes and their types. The output of those checks is still cryptic
* If records are not consistant (e.g. a non record file is present with no attributes), it may still be used for the record creation


tsiyons at iguazio.com
