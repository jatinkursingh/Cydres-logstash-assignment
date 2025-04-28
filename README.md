# Cydres-logstash-assignment
Repo for logstash data ingestion assignment with diffrent input and output method.

**Setup 1** --- ****Normal txt file to json normalization in output only**.

## How It Works
- **Input Plugin**: File input plugin reads the log data from a file stored in servers itself with the provided 
- **Filter Plugins**:
  - `grok` extracts fields using patterns.
  - `mutate` converts severity level from int and removes unnecessary fields.
  - `translate` maps numeric severity levels to readable values.
- **Output Plugin**: Outputs to both console and a `.json` file using JSON codec

**Setup 2**  ----**** **CSV type format ingested to elastic index data in json format and printed out in json using json codec output plugin****
- **Input Plugin**: File input plugin reads the CSV data from a file stored in servers in csv format. 
- **Filter Plugins**:
  - `grok` csv grk filter used to append the data accorind to the column name as utilized.
  - `mutate` converts severity level from int and removes unnecessary fields.
- **Output Plugin**: Outputs to both Elastic setup and json codec for readabilty.

**Result config and other information all are save in the logstash conf and what i used.**
